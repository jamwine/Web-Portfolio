---
# An instance of the Blank widget.
# Documentation: https://wowchemy.com/docs/getting-started/page-builder/
widget: blank

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

design:
# Choose how many columns the section has. Valid values: 1 or 2.
  columns: "1"

# ... Put Your Section Options Here (title etc.) ...
title:
---



<!-- skills section start -->
   <!-- <section class="skills">
          <div class="max-width">
              <h2 class="title">Data Professional</h2>
              <div class="skills-content">
                  <div class="column left">
                      <div class="bars">
                          <div class="info">
                              <span>Machine Learning and Artificial Intelligence</span>
                          </div>
                          <div class="line ml"></div>
                      </div>
                      <div class="bars">
                          <div class="info">
                              <span>Trend Analysis and Predictive Analytics</span>
                          </div>
                          <div class="line trend"></div>
                      </div>
                      <div class="bars">
                          <div class="info">
                              <span>Data Structures & Algorithms</span>
                          </div>
                          <div class="line ds"></div>
                      </div>
                      <div class="bars">
                          <div class="info">
                              <span>Computer Vision techniques</span>
                          </div>
                          <div class="line cv"></div>
                      </div>
                  </div>
                  <div class="column right">
                      <div class="bars">
                          <div class="info">
                              <span>Statistical Modeling and Feature Engineering</span>
                          </div>
                          <div class="line sm"></div>
                      </div>
                      <div class="bars">
                          <div class="info">
                              <span>Data Science and Information Visualization</span>
                          </div>
                          <div class="line iv"></div>
                      </div>
                      <div class="bars">
                          <div class="info">
                              <span>Deep Learning models</span>
                          </div>
                          <div class="line dl"></div>
                      </div>
                      <div class="bars">
                          <div class="info">
                              <span>Web Scraping and Data Mining</span>
                          </div>
                          <div class="line ws"></div>
                      </div>
                  </div>
              </div>
          </div>
      </section> -->

<!-- I am always up for:
 - a cup of delicious coffee
 - dark chocolates
 - discovering new music: [J A M W I N E](https://jam-wine.tumblr.com/)
 - Stock Markets and investments
 - a game of Chess or Table Tennis
 - exploring Open Source Technologies: [Work With Data](https://workwithdata.tumblr.com/)
 - PC Gaming and eSports
 - Coursera MOOCs
 - discussion about new gadgets and PC configurations
 - Logo Designing
 - Traveling (*obviously* :sweat_smile:) -->

<!-- Add a svg area, empty -->
<div id="scatter_area"></div>

<!-- Load d3.js -->
<script src="https://d3js.org/d3.v4.js"></script>

<script>

// set the dimensions and margins of the graph
var margin = {top: 10, right: 40, bottom: 30, left: 30},
    width = 450 - margin.left - margin.right,
    height = 400 - margin.top - margin.bottom;

// append the svg object to the body of the page
var svG = d3.select("#scatter_area")
  .append("svg")
    .attr("width", width + margin.left + margin.right)
    .attr("height", height + margin.top + margin.bottom)
  .append("g")
    .attr("transform",
          "translate(" + margin.left + "," + margin.top + ")");

// Create data
var data = [ {x:10, y:20}, {x:40, y:90}, {x:80, y:50} ]

// X scale and Axis
var x = d3.scaleLinear()
    .domain([0, 100])         // This is the min and the max of the data: 0 to 100 if percentages
    .range([0, width]);       // This is the corresponding value I want in Pixel
svG
  .append('g')
  .attr("transform", "translate(0," + height + ")")
  .call(d3.axisBottom(x));

// X scale and Axis
var y = d3.scaleLinear()
    .domain([0, 100])         // This is the min and the max of the data: 0 to 100 if percentages
    .range([height, 0]);       // This is the corresponding value I want in Pixel
svG
  .append('g')
  .call(d3.axisLeft(y));

// Add 3 dots for 0, 50 and 100%
svG
  .selectAll("whatever")
  .data(data)
  .enter()
  .append("circle")
    .attr("cx", function(d){ return x(d.x) })
    .attr("cy", function(d){ return y(d.y) })
    .attr("r", 7)


</script>