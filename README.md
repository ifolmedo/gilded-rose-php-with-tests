# Gilded Rose Kata in PHP
Starting code for a refactoring and testing code Kata on the Gilded Rose.
The language is PHP (7.2), tested with [PHPUnit](https://phpunit.de/).

## Specification
Hi and welcome to team Gilded Rose. As you know, we are a small inn with a prime location in a prominent city ran by a friendly innkeeper named Allison. We also buy and sell only the finest goods.
Unfortunately, our goods are constantly degrading in quality as they approach their sell by date. We have a system in place that updates our inventory for us. It was developed by a no-nonsense type named
Leeroy, who has moved on to new adventures. Your task is to add the new feature to our system so that we can begin selling a new category of items. First an introduction to our system:

 - All items have a SellIn value which denotes the number of days we have to sell the item
 - All items have a Quality value which denotes how valuable the item is
 - At the end of each day our system lowers both values for every item

Pretty simple, right? Well this is where it gets interesting:

 - Once the sell by date has passed, Quality degrades twice as fast
 - The Quality of an item is never negative
 - "Aged Brie" actually increases in Quality the older it gets
 - The Quality of an item is never more than 50
 - "Sulfuras", being a legendary item, never has to be sold or decreases in Quality
 - "Backstage passes", like aged brie, increases in Quality as it's SellIn value approaches;
   - Quality increases by 2 when there are 10 days or less and by 3 when there are 5 days or less but
   - Quality drops to 0 after the concert
   
Just for clarification, an item can never have its Quality increase above 50, however "Sulfuras" is a legendary item and as such its Quality is 80 and it never alters.

## Requested changes
We have recently signed a supplier of conjured items. This requires an update to our system:

 - "Conjured" items degrade in Quality twice as fast as normal items
 
Note that there are two tests already covering this behavior that had been marked `skipped` (in `ConjuredItemTest`).

Feel free to make any changes to the `updateQuality()` method and add any new code as long as everything still works correctly. However, do not alter the Item class as that code belongs to the goblin in the corner who will insta-rage and one-shot you as he does not believe in shared code ownership.

## Acknowledgements

This Kata was originally created by [Terry Hughes](https://twitter.com/TerryHughes).
[Emily Bache](https://twitter.com/emilybache) translated it to a [few other languages](https://github.com/emilybache/GildedRose-Refactoring-Kata).

She also wrote this article ["Writing Good Tests for the Gilded Rose Kata"](http://coding-is-like-cooking.info/2013/03/writing-good-tests-for-the-gilded-rose-kata/) about how you could use this kata.

This particular version was forked from [@codecop's](https://github.com/codecop) mercurial repo at https://bitbucket.org/pkofler/gilded-rose-kata-php-setup, those commits where preserved in this history. Tests where reworked and the code updated to a PHP 7.2 flavor.

[BSD License](http://opensource.org/licenses/bsd-license.php), see `LICENSE` in repository.
