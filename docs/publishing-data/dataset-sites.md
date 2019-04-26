# Dataset Sites

Dataset Sites help data users find your data, and interact with you if they find any issues. They are both human and machine readable, and allow your data to appear everyone from the [OpenActive Status Page](https://status.openactive.io) to the [Google Dataset Search](https://toolbox.google.com/datasetsearch/search?query=openactive).

### What do I need?

* If you are creating just one Dataset Site for your organisation, then jump to the [Dataset Site Generator](dataset-sites.md#dataset-site-generator).
* If you are a large booking system generating a Dataset Site for each of your customers, jump to the [Dataset Site Template](dataset-sites.md#dataset-site-template).

### What is a Dataset Site?

* A web page that can be referenced when discussing the dataset.
* A human and machine readable licence associated with the data \(the Dataset Site contains invisible metadata which allows its details to be read automatically\).
* A human and machine readable rights statement to specify how dataset users \(innovators who want to build on top of/use your data\) should attribute your data.
* An accessible "single point of truth" that explains where the data can be found.
* Links to documentation relating to the format of the data, including the specifications it follows, and the data fields it contains.
* A place where the community can contribute with comments, and raise issues - all Dataset Sites are linked to a GitHub issues board \(e.g. [this one](https://github.com/gll-better/opendata/issues)\) that allows data users to raise issues in the open.

## Option 1: Dataset Site Generator: Create one Dataset Site

The Dataset Site Generator and associated guides very quickly create a minimal Dataset Site covering all of the criteria above, using freely available, open source tools. A generated site contains features sufficient for publishing a single dataset, which in most cases is enough for initial publishing of data relating to OpenActive.

Please find out more at the [Dataset Site Generator instructions page](https://github.com/openactive/dataset-site-generator/wiki).

{% embed url="https://github.com/openactive/dataset-site-generator/wiki" %}

## Option 2: Dataset Site Template: Build Dataset Sites into your system

The Dataset Site Template is very easy to use and quick to apply - it's basically a single mustache template and associated JSON structure. It is designed to work with minimal effort with an extremely [wide range of platforms and languages](https://mustache.github.io/).

The[ dataset site template repository](https://github.com/openactive/dataset-site-template) contains a [mustache template](https://www.openactive.io/dataset-site-template/datasetsite.mustache) for creating an OpenActive dataset site. This dataset site it produces is slightly more advanced compared with those generated by the Dataset Site Generator.

It is designed to be embedded in a booking system that outputs open data feeds for each customer, and allows the booking system to easily generate a dataset site for each customer.

### Getting Started

The [Dataset Site Template](https://github.com/openactive/dataset-site-template/) is a single self-contained mustache template of an HTML page that contains embedded CSS, an image, and references to [Font Awesome](https://fontawesome.com/) and [Google Fonts](https://fonts.google.com/). It works across all browsers, and includes fully compliant DCAT and schema.org machine-readable metadata to ensure it is compatible with [Google Dataset Search](https://toolbox.google.com/datasetsearch/search?query=openactive).

Steps to render the template:

1. Construct the JSON-LD found in [example.json](https://www.openactive.io/dataset-site-template/example.json) based on your customers' own properties.
2. Find a [mustache library](https://mustache.github.io/) for your platform or language.
3. Write code to do the following:
   * Stringify the input JSON, and place the contents of the string within the "json" property at the root of the JSON itself \(i.e. serialised JSON embedded in the original deserialised object\).
   * Use the resulting JSON with the [mustache template](https://www.openactive.io/dataset-site-template/datasetsite.mustache) to render the dataset site.

### .NET Example

This [simple console app](https://github.com/openactive/dataset-site-template-example-dotnet) demonstrates the render steps outlined above using [OpenActive.NET](https://www.nuget.org/packages/OpenActive.NET/).

{% embed url="https://github.com/openactive/dataset-site-template-example-dotnet" %}

### JavaScript Example

This [JSFiddle](https://jsfiddle.net/nickevansuk/msby0vqg/12/) demonstrates the render steps outlined above using plain JavaScript.

Click the **Result** tab below to see the result of a template render.

{% embed url="https://jsfiddle.net/nickevansuk/msby0vqg/12" %}


