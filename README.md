# Devstratum JQP Graph

jQuery plugin for render simple html block graphs

**Article**

https://devstratum.ru/software/devstratum-jqp-graph-vizualizatsiya-grafikov

## Usage

Include jQuery library

```html
<script src="https://code.jquery.com/jquery-3.4.1.min.js" type="text/javascript"></script>
```

Include local script files in html doc

```html
<link href="css/jquery.dvstr_jqp_graph.css" rel="stylesheet" type="text/css"/>
<script src="js/jquery.dvstr_jqp_graph.js" type="text/javascript"></script>
```
## Example

![screenshot of sample](http://devstratum.ru/images/articles/2019/11/devstratum-jqp-graph-vizualizatsiya-grafikov/devstratum-jqp-graph-vizualizatsiya-grafikov_example.jpg)

```html
<div class="graph-conatainer" id="graph_01"></div>
<script>
    jQuery(document).ready(function($) {
        var color_blue = '#4c8ffc';
        var color_green = '#4f9100';
        var color_orange = '#e76100';

        $('#graph_01').dvstr_graph({
            title: '3DMark 2.7.6',
            description: 'Fire Strike 1920 x 1080 (Radeon RX 470 4GB)',
            unit: 'Score',
            better: 'Higher is better',
            separate: false,
            grid_wmax: 10000,
            grid_part: 10,
            points: [
                {
                    title: 'Combined',
                    color: color_blue
                },
                {
                    title: 'CPU',
                    color: color_green
                },
                {
                    title: 'Overall',
                    color: color_orange
                }
            ],
            graphs: [
                {
                    label: 'Phenom II X6 1055T',
                    color: [
                        color_blue,
                        color_green,
                        color_orange
                    ],
                    value: [
                        3069,
                        5999,
                        8252,
                    ]
                },
                {
                    label: 'Xeon E5450',
                    color: [
                        color_blue,
                        color_green,
                        color_orange
                    ],
                    value: [
                        2863,
                        5120,
                        7927,
                    ]
                },
                {
                    label: 'Core i5-3470',
                    color: [
                        color_blue,
                        color_green,
                        color_orange
                    ],
                    value: [
                        4047,
                        6489,
                        9143,
                    ]
                }
            ]
        });
    });
</script>
```
![screenshot of sample](http://devstratum.ru/images/articles/2019/11/devstratum-jqp-graph-vizualizatsiya-grafikov/devstratum-jqp-graph-vizualizatsiya-grafikov_example-time.jpg)

```html
<div class="graph-conatainer" id="graph_02"></div>
<script>
    jQuery(document).ready(function($) {
        var color_blue = '#4c8ffc';
        var color_red = '#cc0000';

        $('#graph_02').dvstr_graph({
            title: 'Blender 2.79b',
            unit: 'Seconds',
            better: 'Lower is better',
            type: 'time',
            points: [
                {
                    title: 'Samples 150',
                    color: color_blue
                },
                {
                    title: 'Samples 600',
                    color: color_red
                }
            ],
            graphs: [
                {
                    label: 'Phenom II X6 1055T',
                    color: [
                        color_blue,
                        color_red
                    ],
                    value: [
                        '02:19',
                        '09:09'
                    ]
                },
                {
                    label: 'Xeon E5450',
                    color: [
                        color_blue,
                        color_red
                    ],
                    value: [
                        '03:07',
                        '12:22'
                    ]
                },
                {
                    label: 'Core i5-3470',
                    color: [
                        color_blue,
                        color_red
                    ],
                    value: [
                        '01:28',
                        '05:48'
                    ]
                }
            ]
        });
    });
</script>
```

## Options

**title**

* Type: string
* Default: none
* Graph name

**description**

* Type: string
* Default: none
* Graph description

**unit**

* Type: string
* Default: none
* Unit

**better**

* Type: string
* Default: none
* Which values are better, higher or lower

**type**
* Type: string
* Default: number
* Data type, number or time

**separate**

* Type: boolean
* Default: false
* Separating the output of graph rows

**grid_wmax**
* Type: int
* Default: 0
* Maximum range of graph grid units

**grid_part**

* Type: int
* Default: 5
* Number of parts of grid graph

**points**

* Type: object
* Default: none
* An object of points of different dimensions of the graph with the parameters of names and colors

**graphs**

* Type: object
* Default: none
* Graph Row Object with Label, Colors and Value Parameters

## Info

Version: 1.1

License: MIT License

Author: Sergey Osipov

Website: https://devstratum.ru

Email: info@devstartum.ru

Repo: https://github.com/devstratum/Devstratum-JQP-Graph
