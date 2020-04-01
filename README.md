# Scraping-Websites-with-BeautifulSoup


Provided were two files for this project. One is a sample file where we get the sum for testing and the other is the actual data to process for the project.

•	Sample data: http://py4e-data.dr-chuck.net/comments_42.html (Sum=2553)

•	Actual data: http://py4e-data.dr-chuck.net/comments_283324.html (Sum ends with 67)

No need to save these files to your folder since your program will read the data directly from the URL.


Data Format

The file is a table of names and comment counts.Ignored most of the data in the file except for lines like the following:
<tr><td>Modu</td><td><span class="comments">90</span></td></tr>

<tr><td>Kenzie</td><td><span class="comments">88</span></td></tr>

<tr><td>Hubert</td><td><span class="comments">87</span></td></tr>

Found all the <span> tags in the file and pulled out the numbers from the tag and sum the numbers.



# Retrieved all of the anchor tags

tags = soup('a')

for tag in tags:

# Looked at the parts of a tag

print 'TAG:',tag

print 'URL:',tag.get('href', None)

print 'Contents:',tag.contents[0]

print 'Attrs:',tag.attrs
