# Waiter, there's a fly in my soup!

Our visualization of restaurant inspection scores in the South Bay can be found on the web at http://parkmichelle.github.io/flyinsoup. To view it locally, navigate to the unzipped directory, run a python server using python3 -m http.server, and view localhost:8000 in your browser.

## Time spent
We spent about 30 hours total.

## Division of work
We divided the work evenly, splitting large tasks into smaller milestones that we each worked on, and collaborated through Github.

## Aspects that took most time
Enabling rapid data update during drag took the most time. We went through several iterations of code design, from experimenting with using enter() and exit() to only draw points once, to passing arguments into a drag callback, before landing on our final solution (drawing the intersection points and non-intersection points in two separate calls). 

## Design Decisions
We built this visualization with the following user in mind: someone who is generally familiar with the South Bay wants to explore restaurants near two locations (maybe their home and work), but they also care about cleanliness of the establishment (health inspection score).

We chose to encode inspection scores with both color and text, since many scores occur within a small range of high values (appearing to be very similar shades of green on the map). We chose not to display restaurants that were missing inspection scores. We also added information on restaurant grade in the hover menu, so users can interpret the inspection score more easily. 

Restaurant names are displayed in the hover text and are also searchable. When the two spotlights are displayed, name search only highlights results in the intersection of both spotlights. The search is live and filters results character-by-character, so users can instantly see that a search is happening even if there are no results in the intersection. We also decided to give users the option to turn off both spotlights, which allows them to search the entire map and view scores at a glance. 

Rather than label the spotlights individually on the map (which we found to be visually clunky), the radius controls match the initial positions of the spotlights, implicitly labeling them left and right with respect to the default spotlight positions. We display radius in miles rather than pixels to allow for more intuitive adjustments.

## Note
This visualization was designed for a 15-inch screen. It is compatible with smaller screens, but some hover text at the edges of the map may get clipped.

