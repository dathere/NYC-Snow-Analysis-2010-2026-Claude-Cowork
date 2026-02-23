# NYC Snow Analysis 2010-2026 with Claude Cowork

![NYC Snow Response Analysis](./images/snow-related-311-complaints-2010-26.png)

What do you get when you unleash [Claude Cowork](https://claude.com/product/cowork) on:

* [All of NYC 311 Service Requests](https://opendata.cityofnewyork.us/311-service-requests-from-2010-to-present-updates/) covering 2010 to 2026-02-22 - **all 24.1gb with 42,873,338 rows!!!**
* NYC's [DCP Housing Database (Inactives Included) from 2010-2025](https://www.nyc.gov/content/planning/pages/resources/datasets/housing-project-level) with 106,358 rows and its Data Dictionary

And install in Cowork:
* our [qsv MCP Server](https://github.com/dathere/qsv)
* the [US Census MCP Server](https://github.com/uscensusbureau/us-census-bureau-data-api-mcp)
* the [Open-Meteo Weather MCP Server](https://github.com/cmer81/open-meteo-mcp)

## The Prompt

You get to ask questions like this:

```
Can you analyze the NYC 311 file as well as the Housing Database (consult the
Data Dictionary PDF) and retrieve from the web all the snowstorms in NYC
since 2010, the current weather details during the snowstorm, NYC news
coverage about the City's handling for each snow event, further enriching it
with Census Data and glean from your detailed temporal analysis any
interesting insights that can be shared with the current administration?
```

## The Results

And 34 minutes later, we get a comprehensive analysis of NYC's snow response over the last 16 years, complete with data visualizations, insights, and recommendations for future improvements:

* [NYC_Snow_Response_Analysis.html](./reports/NYC_Snow_Response_Analysis.html)
* [NYC_Snow_Response_Analysis.docx](./reports/NYC_Snow_Response_Analysis.docx) ([pdf](./reports/NYC_Snow_Response_Analysis-docx.pdf))
* [NYC_Snow_Response_Briefing.pptx](./reports/NYC_Snow_Response_Briefing.pptx) ([pdf](./reports/NYC_Snow_Response_Briefing-slides.pdf))

The full transcript of the Cowork session is available [here](./NYC%20Snow%20Response%20Analysis%20-%20Cowork%20Transcript.md).

## Follow-up Question

```
Can you also do an extended temporal analysis on related snow-related
complaint types (e.g. heating, shelter, frozen pipes, etc.) over the same period
using both datasets, leveraging historical weather data and the Census?
```

32 minutes later, we get these additional insights and visualizations:

* [NYC_Snow_Adjacent_Analysis.html](./reports/NYC_Snow_Adjacent_Analysis.html)
* [NYC_Snow_Adjacent_Analysis.docx](./reports/NYC_Snow_Adjacent_Analysis.docx) ([pdf](./reports/NYC_Snow_Adjacent_Analysis-docx.pdf))
* [NYC_Snow_Adjacent_Briefing.pptx](./reports/NYC_Snow_Adjacent_Briefing.pptx) ([pdf](./reports/NYC_Snow_Adjacent_Briefing-slides.pdf))

## Conclusion

This experiment demonstrates the power of Claude Cowork to handle large datasets, integrate multiple data sources, and produce comprehensive analyses and deliverables in a fraction of the time it would take a human analyst. With the right prompt and access to relevant data, Cowork can generate insights that can inform policy decisions and improve public services.

BUT, how can we be sure the insights are valid? How can we verify the accuracy of the analysis and the quality of the deliverables? This is where human judgment and expertise still play a crucial role. Cowork can do the heavy lifting of data processing and initial analysis, but humans need to review, validate, and interpret the results to ensure they are actionable and meaningful.

That's why we call it **_"Accelerated Civic Intelligence (ACI)"_** - it's not about replacing human analysts, but about augmenting their capabilities and accelerating the process of generating insights that can drive positive change in our cities.

If "computers are the bicycle for the mind", then AI tools like Claude Cowork are more like an Iron Man suit: they dramatically extend our reach, strength, and speed. But even the most advanced suit still needs a capable pilot. The technology can amplify our abilities — it’s human judgment, experience, and civic responsibility that determine where we go and why.
