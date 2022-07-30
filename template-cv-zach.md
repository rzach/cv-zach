---
citation-style: chicago-author-date.csl
nocite: |
  @*
...


# $name$

$for(address)$
>  $address$
$endfor$

> Web: [$www$](http://$www$) 
> EMail: [$email$](mailto:$email$)
> Phone: $tel$
> Twitter: [$twitter$](http://twitter.com/$twitter$)
> [Google Scholar](https://scholar.google.ca/citations?user=$scholar$&hl=en&oi=ao)
> [Philpapers](https://philpapers.org/profile/$philpapers$)
> ORCID: [$orcid$](http://orcid.org/$orcid$)


## Education

$for(education)$
$education.degree$, **$education.school$**, $education.field$, $education.date$
$if(education.info)$
$for(education.info)$
$if(education.info.text)$
% Store certain things in a field called 'text' to allow another field
% for priority.
$education.info.text$
$else$

- $education.info$
$endif$
$endfor$
$endif$

$endfor$

## Appointments

$for(appointment)$
### $appointment.place$

$for(appointment.items)$
$appointment.items.item$. $appointment.items.begindate$-$if(appointment.items.enddate)$$appointment.items.enddate$$endif$.

$endfor$
$endfor$

## Awards

$for(award)$
$award.title$, $award.agency$, $award.date$.

$endfor$

## Editor

$for(editor)$
_[$editor.item$]($editor.link$)_, $editor.role$. $editor.begindate$-$if(editor.enddate)$$editor.enddate$$endif$.

$endfor$

## Publications

::: {#refs}
:::

## Invited Talks

$for(presentation)$
$if(presentation.invited)$$presentation.title$. $if(presentation.host)$$presentation.host$, $endif$$presentation.place$, $presentation.date$.

$endif$$endfor$

## Keynotes

$for(presentation)$
$if(presentation.keynote)$$presentation.title$. $if(presentation.host)$_$presentation.host$_, $endif$$presentation.place$, $presentation.date$.

$endif$$endfor$

## Invited Workshops

$for(presentation)$
$if(presentation.workshop)$$presentation.title$. $if(presentation.host)$_$presentation.host$_, $endif$$presentation.place$, $presentation.date$.

$endif$$endfor$

## Conference Talks

$for(presentation)$
$if(presentation.conference)$$presentation.title$. $if(presentation.host)$_$presentation.host$_, $endif$$presentation.place$, $presentation.date$.

$endif$$endfor$

## Graduate Supervision

$for(students)$
#### $students.type$
$for(students.students)$
$if(students.students.webpage)$[$students.students.name$]($students.students.webpage$)$else$$students.students.name$$endif$ ($students.students.degree$), "$if(students.students.link)$[$students.students.thesis$]($students.students.link$)$else$$students.students.thesis$$endif$," $students.students.date$

$endfor$
$endfor$


### Teaching Awards

$for(teaching-award)$
$teaching-award.title$, $teaching-award.agency$, $teaching-award.date$.

$endfor$
