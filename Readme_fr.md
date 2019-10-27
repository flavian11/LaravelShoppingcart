## LaravelShoppingcart
[![Build Status](https://travis-ci.org/bumbummen99/LaravelShoppingcart.png?branch=master)](https://travis-ci.org/bumbummen99/LaravelShoppingcart)
[![codecov](https://codecov.io/gh/bumbummen99/LaravelShoppingcart/branch/master/graph/badge.svg)](https://codecov.io/gh/bumbummen99/LaravelShoppingcart)
[![StyleCI](https://styleci.io/repos/152610878/shield?branch=master)](https://styleci.io/repos/152610878)
[![Total Downloads](https://poser.pugx.org/bumbummen99/shoppingcart/downloads.png)](https://packagist.org/packages/bumbummen99/shoppingcart)
[![Latest Stable Version](https://poser.pugx.org/bumbummen99/shoppingcart/v/stable)](https://packagist.org/packages/bumbummen99/shoppingcart)
[![Latest Unstable Version](https://poser.pugx.org/bumbummen99/shoppingcart/v/unstable)](https://packagist.org/packages/bumbummen99/shoppingcart)
[![License](https://poser.pugx.org/bumbummen99/shoppingcart/license)](https://packagist.org/packages/bumbummen99/shoppingcart)

Ce projet est un fork de [Crisane's LaravelShoppingcart](https://github.com/Crinsane/LaravelShoppingcart) avec quelques fonctionnalitées compatible avec Laravel 6.

## Installation

Installez le [package](https://packagist.org/packages/bumbummen99/shoppingcart) avec [Composer](http://getcomposer.org/). 

Lancer la commande Composer require depuis votre terminal;

    composer require bumbummen99/shoppingcart

Vous êtes maintenant prêt à utiliser shoppingcart dans votre application.

**Depuis la version 2 de ce package, il est possible d'utiliser l'injection de dépendence pour injeter une instance de la class Cart dans votre controller ou dans une autre class**

## Sommaire
Regardez un de ces sujets pour en apprendre plus à propos de LaravelShoppingcart

* [Usage](#usage)
* [Collections](#collections)
* [Instances](#instances)
* [Models](#models)
* [Database](#database)
* [Exceptions](#exceptions)
* [Events](#events)
* [Example](#example)

## Usage

La class shoppingcart vous permet d'utiliser ces methodes suivantes:

### Cart::add()

Ajouter un objet à une cart est très simple, il suffit simplement d'utiliser la methode `add()` qui accepte différents paramètres.

Dans sa forme la plus basique, vous pouvez spécifier l'id, le nom, la quantité, le prix, et le poid du produit que vous voulez ajouter à la cart.

```php
Cart::add('293ad', 'Product 1', 1, 9.99, 550);
```

Comme cinquième paramètre optionnel vous pouvez donner des options, de façon à pouvoir ajouter plusieurs objets avec le même id, mais avec (dans cet exemple) une taille différente.

```php
Cart::add('293ad', 'Product 1', 1, 9.99, 550, ['size' => 'large']);
```

**La methode `add()` retourne une instance de CartItem de l'etime que vous venez d'ajouter à la carte.**
