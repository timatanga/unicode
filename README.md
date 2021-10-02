# Utilities

This package provides common utility capabilities for PHP applications. 

One set of utility classes is focused on International Components for Unicode (ICU ) datasets. For the following components, default ICU datasets are available as configuration files:
- Locales
- Currencies
- Timezones



## Installation
composer require timatanga/unicode



## Basic Usage International Components for Unicode (ICU)

While creating instances of utility classes, default datasets are loaded from config files.

	// create new currency class loads default configuration
	$currencies = new Currency();
	$locales = new Locale();
	$timezones = new Timezone();


Datasets are searchable with key value pairs

	// search for datasets
	$currency = $currencies->search('code', 'USD']);
	$locale = $locales->search('code', 'de']);



## Custom Usage International Components for Unicode (ICU)

Custom utility datasets can be loaded via the constructor method. Custom datasets must comply to the internal data structure

	// create new currency class with custom dataset 
	$currencies = new Currency([...]);
	$locales = new Locale([...]);
	$timezones = new Timezone([...]);


