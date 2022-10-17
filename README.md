# HTML_Introduction_2

Introduction to HTML for Web2 beginners.

If you're that means you have completed the HTML Introduction Part 1.

In this section, you will learn how to create tables in HTML.

# Introduction to Tables

There are many websites on the Internet that display information like stock prices, sports scores, invoice data, and more. This data is tabular in nature, meaning that a table is often the best way of presenting the data.

In this part of the course, we’ll learn how to use the HTML ```<table>``` element to present information in a two-dimensional table to the users.

Let’s get started!

## Class work

Put this code inside your new index.txt file and see how it renders.


```
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>

  <table>
    <thead>
      <tr>
        <th>Company Name</th>
        <th>Number of Items to Ship</th>
        <th>Next Action</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Adam's Greenworks</th>
        <td>14</td>
        <td>Package Items</td>
      </tr>
      <tr>
        <th>Davie's Burgers</th>
        <td>2</td>
        <td>Send Invoice</td>
      </tr>
      <tr>
        <th>Baker's Bike Shop</th>
        <td>3</td>
        <td>Send Invoice</td>
      </tr>
      <tr>
        <th>Miss Sally's Southern</th>
        <td>4</td>
        <td>Ship</td>
      </tr>
      <tr>
        <th>Summit Resort Rentals</th>
        <td>4</td>
        <td>Ship</td>
      </tr>
      <tr>
        <th>Strike Fitness</th>
        <td>1</td>
        <td>Enter Order</td>
      </tr>
      </tbody>
  </table>

</body>
</html>
```

Take time to look through the code, we're going to break it down soon.


# Create a Table

Before displaying data, we must first create the table that will contain the data by using the ```<table>``` element.

```
<table>
 
</table>
```


## Class work

Open a new index.txt file, write all your basic HTML elements(HTML, Head, Title, and Body)

Inside the body, insert a table element inside the body element.



# Table Rows

In many programs that use tables, the table is already predefined for you, meaning that it contains the rows, columns, and cells that will hold data. In HTML, all of these components must be created.

The first step in entering data into the table is to add rows using the table row element: ```<tr>```. like this:

```
<table>
  <tr>
  </tr>
  <tr>
  </tr>
</table>
```

In the example above, two rows have been added to the table.

## Class work

In your index.txt file, add two rows to the table element you just created.


Your index.txt should be:

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

</tr>

<tr>

</tr>

</table>

</body>

</html>
```


# Table Data

Rows aren’t sufficient to add data to a table. Each cell element must also be defined. In HTML, you can add data using the table data element: ```<td>```.

```
<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

In the example above, two data points (73 and 81) were entered in the one row that exists. By adding two data points, we created two cells of data.

## Class work

In your index.txt file, in the second row you created, add three cells of data. The cells should contain the following data, in order:

- Adam’s Greenworks
- 14
- Package Items

Your index.txt file:

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

</tr>

<tr>

<td>
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

</table>

</body>

</html>
```


# Table Headings

Table data doesn’t make much sense without titles to describe what the data represents.

To add titles to rows and columns, you can use the table heading element: ```<th>```.

Just like table data, a table heading must be placed within a table row. Like:

```
<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

First, a new row was added to hold the three headings: 

- a blank heading, 
- a Saturday heading, 
- and a Sunday heading. 

The blank heading creates the extra table cell necessary to align the table headings correctly over the data they correspond to.

In the second row, one table heading was added as a row title: Temperature.

When rendered, this code will appear similar to the image below:

![Screenshot 2022-10-17 at 13 43 39](https://user-images.githubusercontent.com/29931071/196181940-547cd497-433f-494b-b27a-f594b37f0aba.png)

Note, also, the use of the scope attribute, which can take one of two values:

- row - this value makes it clear that the heading is for a row.

- col - this value makes it clear that the heading is for a column.

## Class work

1. In the first row, add three table headings. The headings should contain the following data, in order:

- Company Name
- Number of Items to Ship
- Next Action

Index.txt = 

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

<th>Company Name</th>
<th>Number of Items to Ship</th>
<th>Next Action</th>

</tr>

<tr>

<td>
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

</table>

</body>

</html>
```

2. Now add a scope attribute to each of these new headings.

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>

<tr>

<td>Adam’s Greenworks</td>

<td>14</td>

<td>Package Items</td>

</tr>

</table>

</body>

</html>
```


# Table Borders

So far, the tables you’ve created have been a little difficult to read because they have no borders.

In older versions of HTML, a border could be added to a table using the ```border``` attribute and setting it equal to an integer. This integer would represent the thickness of the border. Like:

```
<table border="1">
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```

The code in the example above is deprecated, so please don’t use it. It’s meant to illustrate older conventions you may come across when reading other developers’ code.

The browser will likely still interpret your code correctly if you use the border attribute, but that doesn’t mean the attribute should be used.

We use CSS to add style to HTML documents, because it helps us to separate the structure of a page from how it looks. You will learn more about CSS in the CSS section of this class which comes next.

You can achieve the same table border effect using CSS:

```
table, td {
  border: 1px solid black;
}
```

## Class work

1 We’re going to need some more data in the table. Add the following data to the table. Make sure to place it after the second table row.

```
<tr>
  <td>Davie's Burgers</td>
  <td>2</td>
  <td>Send Invoice</td>
</tr>
<tr>
  <td>Baker's Bike Shop</td>
  <td>3</td>
  <td>Send Invoice</td>
</tr>
```


Therefore index.txt will look like this:

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>

<tr>

<td>
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

<tr>

<td>Davie's Burgers</td>
<td>2</td>
<td>Send Invoice</td>

</tr>
<tr>

<td>Baker's Bike Shop</td>
<td>3</td>
<td>Send Invoice</td>

</tr>

</table>

</body>

</html>
```

2. Open a new txt document and name it style.css.

Inside the style.css file, write:

```
table {
  height: 40%;
  left: 10%;
  margin: 20px auto;
  overflow-y: scroll;
  position: static;
  width: 80%;
}

thead th {
  background: #88CCF1;
  color: #FFF;
  font-family: 'Lato', sans-serif;
  font-size: 16px;
  font-weight: 100;
  letter-spacing: 2px;
  text-transform: uppercase;
}

tr {
  background: #f4f7f8;
  border-bottom: 1px solid #FFF;
  margin-bottom: 5px;
}

th, td {
  font-family: 'Lato', sans-serif;
  font-weight: 400;
  padding: 20px;
  text-align: left;
  width: 33.3333%;
}
```

3. Go back to the index.txt file and add this line of code inside the head element:

```
<link href="style.css" type="text/css" rel="stylesheet" />
```


# Spanning Columns

What if the table contains data that spans multiple columns?

For example, a personal calendar could have events that span across multiple hours, or even multiple days.

Data can span columns using the colspan attribute. The attribute accepts an integer (greater than or equal to 1) to denote the number of columns it spans across. For example:

![Screenshot 2022-10-17 at 14 08 37](https://user-images.githubusercontent.com/29931071/196187134-82add6e3-4415-49df-b5db-2b64ffc8d3a0.png)


## Class work

Span Adam's greenworks into two columns - Company name and number of items to ship.

Index.txt should be:

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>

<tr>

<td colspan="2">
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

<tr>

<td>Davie's Burgers</td>
<td>2</td>
<td>Send Invoice</td>

</tr>
<tr>

<td>Baker's Bike Shop</td>
<td>3</td>
<td>Send Invoice</td>

</tr>

</table>

</body>

</html>
```


# Spanning Rows

Data can also span multiple rows using the rowspan attribute.

The rowspan attribute is used for data that spans multiple rows (perhaps an event goes on for multiple hours on a certain day). It accepts an integer (greater than or equal to 1) to denote the number of rows it spans across.

![Screenshot 2022-10-17 at 14 14 08](https://user-images.githubusercontent.com/29931071/196188329-56204ad2-b3c0-4643-ac7e-d793d72f51df.png)


## Class work

Rowspan "Davie's Burgers"

Index.txt file will be:


```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>

<tr>

<td colspan="2">
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

<tr>

<td rowspan="2">Davie's Burgers</td>
<td>2</td>
<td>Send Invoice</td>

</tr>
<tr>

<td>Baker's Bike Shop</td>
<td>3</td>
<td>Send Invoice</td>

</tr>

</table>

</body>

</html>
```

# Table Body

Over time, a table can grow to contain a lot of data and become very long. When this happens, the table can be sectioned off so that it is easier to manage.

Long tables can be sectioned off using the table body element: ```<tbody>```.

The ```<tbody>``` element should contain all of the table’s data, excluding the table headings (more on this in a later exercise). Like:

```
<table>
  <tbody>
    <tr>
      <th></th>
      <th>Saturday</th>
      <th>Sunday</th>
    </tr>
    <tr>
      <th>Morning</th>
      <td rowspan="2">Work</td>
      <td rowspan="3">Relax</td>
    </tr>
    <tr>
     <th>Afternoon</th>
    </tr>
    <tr>
      <th>Evening</th>
      <td>Dinner</td>
    </tr>
  </tbody>
</table>
```


## Class work

Enclose rows 2, 3, and 4 of the table in a <tbody> element.

Index.txt will now be:

```

<html>

<head>

<title>

</title>

</head>

<body>

<table>

<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>

<tbody>
<tr>

<td colspan="2">
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

<tr>

<td rowspan="2">Davie's Burgers</td>
<td>2</td>
<td>Send Invoice</td>

</tr>
<tr>

<td>Baker's Bike Shop</td>
<td>3</td>
<td>Send Invoice</td>

</tr>

</tbody>

</table>

</body>

</html>
```


# Table Head

In the last exercise, the table’s headings were kept inside of the table’s body. When a table’s body is sectioned off, however, it also makes sense to section off the table’s column headings using the <thead> element. Example:

```
<table>
  <thead>
    <tr>
      <th></th>
      <th scope="col">Saturday</th>
      <th scope="col">Sunday</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Morning</th>
      <td rowspan="2">Work</td>
      <td rowspan="3">Relax</td>
    </tr>
    <tr>
     <th scope="row">Afternoon</th>
    </tr>
    <tr>
      <th scope="row">Evening</th>
      <td>Dinner</td>
    </tr>
  </tbody>
</table>
```

Additionally, only the column headings go under the <thead> element.


## Class work

Enclose the first row of the table in a <thead> element.

Index.txt will now be:

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<thead>
<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>
</thead>

<tbody>
<tr>

<td colspan="2">
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

<tr>

<td rowspan="2">Davie's Burgers</td>
<td>2</td>
<td>Send Invoice</td>

</tr>
<tr>

<td>Baker's Bike Shop</td>
<td>3</td>
<td>Send Invoice</td>

</tr>

</tbody>

</table>

</body>

</html>
```

# Table Footer

The bottom part of a long table can also be sectioned off using the ```<tfoot>``` element. Like:

```
<tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
```

## Class work

Add a table footer at the bottom of the table using the <tfoot> element. Inside of the footer, add the following data:

```
<td>Total</td>
<td>28</td>
```

Index.txt will now be:

```
<html>

<head>

<title>

</title>

</head>

<body>

<table>

<thead>
<tr>

<th scope="col">Company Name</th>
<th scope="col">Number of Items to Ship</th>
<th scope="col">Next Action</th>

</tr>
</thead>

<tbody>
<tr>

<td colspan="2">
Adam’s Greenworks
</td>

<td>
14
</td>

<td>
Package Items
</td>

</tr>

<tr>

<td rowspan="2">Davie's Burgers</td>
<td>2</td>
<td>Send Invoice</td>

</tr>
<tr>

<td>Baker's Bike Shop</td>
<td>3</td>
<td>Send Invoice</td>

</tr>

</tbody>

<tfoot>

<td>Total</td>
<td>28</td>

</tfoot>

</table>

</body>

</html>
```

# Styling with CSS

Tables, by default, are very bland. They have no borders, the font color is black, and the typeface is the same type used for other HTML elements.

CSS, or Cascading Style Sheets, is a language that web developers use to style the HTML content on a web page. You can use CSS to style tables. Specifically, you can style the various aspects mentioned above. For example:


```
table, th, td {
  border: 1px solid black;
  font-family: Arial, sans-serif;
  text-align: center;
}
```

## Class work:

We’ve included a .css file containing instructions for styling the HTML content in the index.html file.

In style.css, set the font-size of all table headings (th) and table data (td) to 18 pixels (18px).

Copy this code into your style.css file:

```
body {
  background: #EEE;
  margin: 0;
  padding: 0;
}

table {
  height: 40%;
  left: 10%;
  margin: 20px auto;
  overflow-y: scroll;
  position: static;
  width: 80%;
}

thead th {
  background: #88CCF1;
  color: #FFF;
  font-family: 'Lato', sans-serif;
  font-size: 16px;
  font-weight: 100;
  letter-spacing: 2px;
  text-transform: uppercase;
}

tr {
  background: #f4f7f8;
  border-bottom: 1px solid #FFF;
  margin-bottom: 5px;
}

th, td {
  font-family: 'Lato', sans-serif;
  font-size: 18px;
  font-weight: 400;
  padding: 20px;
  text-align: left;
  width: 33.3333%;
}
```
