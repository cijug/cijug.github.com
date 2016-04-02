---
layout: post
title: "Rolling back Spring Transactions in Cucumber-JVM"
date: 2012-12-04 15:10
comments: true
categories: tech
---

I recently spent a lot more time than I should getting Cucumber-JVM to
roll back my Spring db transactions. Thanks to
[SpringTransactionHooks][1] its already there, but not very well documented. Here's how I made it work.

RunCukesTest.java
-----------------

{% highlight java linenos %}
package org.cijug.cukes;

import cucumber.api.junit.Cucumber;
import org.junit.runner.RunWith;

@RunWith(Cucumber.class)
@Cucumber.Options(glue = {"org.cijug.cukes", "cucumber.api.spring"})
public class RunCukesTest {
}
{% endhighlight %}

Check out line 7, he's the important one. He tells Cucumber where to
find our feature files and rollback our spring transactions 

chores.feature
--------------

{% highlight gherkin linenos %}
@txn
Feature: Get paid for chores
  Scenario: Give a dollar for each chore
    Given son has done the following chores:
      | chore             |
      | Raked leaves      |
      | Put away laundry  |
      | Washed the dishes |
    Then he should get "3" dollars

  Scenario: Give two dollars for each chore
    Given son has done the following chores:
      | chore             |
      | Raked leaves      |
      | Put away laundry  |
      | Washed the dishes |
    Then he should get "6" dollars
{% endhighlight %}

Check out line 1. Without the @txn annotation, this test does not pass.

applicationContext.xml
----------------------

{% highlight xml %}
<bean id="transactionManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">
    <property name="dataSource" ref="dataSource"/>
</bean>
{% endhighlight %}

This is pretty obvious, but you can't roll back a transaction if you
don't have a transaction manager.

This feature only passes because Cucumber rolls the transaction back after each scenario. If he didn't, the second scenario would pay out a lot more than $6. If you remove the @txn from the feature file, see what happens.

[1]: http://cukes.info/api/cucumber/jvm/javadoc/cucumber/api/spring/SpringTransactionHooks.html

