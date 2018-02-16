---
title: "xPDOQuery.andCondition"
_old_id: "1290"
_old_uri: "2.x/class-reference/xpdoquery/xpdoquery.andcondition"
---

xPDOQuery::andCondition
-----------------------

Add an AND condition to the WHERE clause.

Syntax
------

API Docs: [http://api.modx.com/revolution/2.2/db\_core\_xpdo\_om\_xpdoquery.class.html#\\xPDOQuery::andCondition()](http://api.modx.com/revolution/2.2/db_core_xpdo_om_xpdoquery.class.html#xPDOQuery::andCondition())

```
<pre class="brush: php">
void andCondition ( $conditions, [ $binding = null], [ $group = 0])

```Example
-------

Grab all Boxes with width of 12 and height of 4.

```
<pre class="brush: php">
$query = $xpdo->newQuery('Box');
$query->where(array('width' => 12));
$query->andCondition(array('height' => 4));
$boxes = $xpdo->getCollection('Box',$query);

```<div class="warning">**Warning**  
The order you call the functions is important! The **andCondition** must come after the **where** method has been used.</div>See Also
--------

- [xPDOQuery](/xpdo/2.x/class-reference/xpdoquery "xPDOQuery")