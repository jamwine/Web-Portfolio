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


<style>
#content{
    padding: 20px;
    /* width: 500px;
   height: 500px; */
}
.left{
    display: inline-block;
    box-sizing: border-box;
    width: 45%;
    height: 100%;
    margin-right: 50px;
}
.right{
    display: inline-block;
    box-sizing: border-box;
    width: 45%;
    height: 100%;
}
</style>

<!-- Load d3.js -->
<script src="https://d3js.org/d3.v4.js"></script>

<!-- Create a div where the graph will take place -->
<div id="content">
    <div id="my_dataviz" class="left"></div>
    <div id="my_dataviz2" class="right"></div>
 </div>

<script>

// set the dimensions and margins of the graph
var margin = {top: 10, right: 30, bottom: 90, left: 40},
    width = 460 - margin.left - margin.right,
    height = 450 - margin.top - margin.bottom;

// append the svg object to the body of the page
var svg = d3.select("#my_dataviz")
  .append("svg")
    .attr("width", width + margin.left + margin.right)
    .attr("height", height + margin.top + margin.bottom)
  .append("g")
    .attr("transform",
          "translate(" + margin.left + "," + margin.top + ")");

// Parse the Data
d3.csv("https://raw.githubusercontent.com/holtzy/data_to_viz/master/Example_dataset/7_OneCatOneNum_header.csv", function(data) {

// X axis
var x = d3.scaleBand()
  .range([ 0, width ])
  .domain(data.map(function(d) { return d.Country; }))
  .padding(0.2);
svg.append("g")
  .attr("transform", "translate(0," + height + ")")
  .call(d3.axisBottom(x))
  .selectAll("text")
    .attr("transform", "translate(-10,0)rotate(-45)")
    .style("text-anchor", "end");

// Add Y axis
var y = d3.scaleLinear()
  .domain([0, 13000])
  .range([ height, 0]);
svg.append("g")
  .call(d3.axisLeft(y));

// Bars
svg.selectAll("mybar")
  .data(data)
  .enter()
  .append("rect")
    .attr("x", function(d) { return x(d.Country); })
    .attr("width", x.bandwidth())
    .attr("fill", "#69b3a2")
    // no bar at the beginning thus:
    .attr("height", function(d) { return height - y(0); }) // always equal to 0
    .attr("y", function(d) { return y(0); })

// Animation
svg.selectAll("rect")
  .transition()
  .duration(800)
  .attr("y", function(d) { return y(d.Value); })
  .attr("height", function(d) { return height - y(d.Value); })
  .delay(function(d,i){console.log(i) ; return(i*100)})

})


// set the dimensions and margins of the graph
var margin = {top: 10, right: 30, bottom: 40, left: 100},
    width = 460 - margin.left - margin.right,
    height = 500 - margin.top - margin.bottom;

// append the svg object to the body of the page
var svg = d3.select("#my_dataviz2")
  .append("svg")
    .attr("width", width + margin.left + margin.right)
    .attr("height", height + margin.top + margin.bottom)
  .append("g")
    .attr("transform",
          "translate(" + margin.left + "," + margin.top + ")");

// Parse the Data
d3.csv("https://raw.githubusercontent.com/holtzy/data_to_viz/master/Example_dataset/7_OneCatOneNum_header.csv", function(data) {

// sort data
data.sort(function(b, a) {
  return a.Value - b.Value;
});

// Add X axis
var x = d3.scaleLinear()
  .domain([0, 13000])
  .range([ 0, width]);
svg.append("g")
  .attr("transform", "translate(0," + height + ")")
  .call(d3.axisBottom(x))
  .selectAll("text")
    .attr("transform", "translate(-10,0)rotate(-45)")
    .style("text-anchor", "end");

// Y axis
var y = d3.scaleBand()
  .range([ 0, height ])
  .domain(data.map(function(d) { return d.Country; }))
  .padding(1);
svg.append("g")
  .call(d3.axisLeft(y))

// Lines
svg.selectAll("myline")
  .data(data)
  .enter()
  .append("line")
    .attr("x1", x(0))
    .attr("x2", x(0))
    .attr("y1", function(d) { return y(d.Country); })
    .attr("y2", function(d) { return y(d.Country); })
    .attr("stroke", "grey")

// Circles -> start at X=0
svg.selectAll("mycircle")
  .data(data)
  .enter()
  .append("circle")
    .attr("cx", x(0) )
    .attr("cy", function(d) { return y(d.Country); })
    .attr("r", "7")
    .style("fill", "#69b3a2")
    .attr("stroke", "black")

// Change the X coordinates of line and circle
svg.selectAll("circle")
  .transition()
  .duration(2000)
  .attr("cx", function(d) { return x(d.Value); })

svg.selectAll("line")
  .transition()
  .duration(2000)
  .attr("x1", function(d) { return x(d.Value); })

})

</script>