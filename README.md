# Polygon Angle Lab

Polygon Angle Lab is a practice app for the interior angle sum of a polygon. Students triangulate generated convex polygons from one vertex, predict the triangle count and the angle sum before each reveal, and watch a pattern table accumulate across side counts until they state the rule, (n - 2) x 180, in their own words and the app confirms it. After the derivation, three drill modes run the rule in every direction the indicator demands: sum from sides, sides from sum, regular interior and exterior angles, and the inverse trip from a regular interior angle back to the side count. Every drill carries a predict-first step: a committed prediction is required before an answer can be checked.

Math 2201 Unit 8: Properties of Angles and Triangles (indicator 5.5)

## How students use it

- Triangulate and Derive: choose a side count (3 to 12) or take a surprise polygon, predict, triangulate, and add a row to the pattern table. After three different side counts, the app asks for the rule in the student's own words before revealing the general statement to compare against.
- Run the Rule Both Ways: sums from sides and sides from sums, alternating.
- Regular Angles: one interior angle, one exterior angle, and sides from a given interior angle, over side counts chosen so every angle is a whole number of degrees.
- Lesson 2 Practice Set: all six question kinds mixed. The Section 4 pacing note folds Lesson 2 into one lesson if needed and promises that this app carries Lesson 2's both-ways practice; this set is that promise, labelled as such in the app.

The Generalization Record at the bottom collects the triangulation table, the rule in the student's own words with the confirmed general rule beside it, and the practice completed. The Section 4 portfolio asks for this record.

## Technical notes

Single HTML file, no dependencies, works offline. All logic is inline in index.html, generation is seeded and reproducible, and a Node harness (harness.js) verifies the geometry independently: drawn polygons are re-checked for convexity and their interior angles re-measured from the coordinates with atan2 to confirm the sum, drill keys are re-derived from the closed forms with prompt givens parsed back out of the text, and the Lesson 2 set is proven to serve all six kinds. Regular-polygon drills only use side counts whose interior and exterior angles are whole degrees. Nothing is recorded and nothing leaves the page.

GitHub topics when published: math-2201, angles-triangles, draft (draft removed after QA).
