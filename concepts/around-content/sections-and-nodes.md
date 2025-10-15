The header menu shows sections per the definition in data_site.tsv.

These may be grouped per syntax "group: a+b" and are comma separated.

Framework's site.php interprets this heterogeneous definition which is primarily a csv line.

The htaccess configures the url as node then page parameter(s), per the interpretation in entry.php.

If root of site, and empty, the node is set to index, which file is looked for in "content" main folder. See render() for details on how it searches for fwk/cms or site's cms to resolve the current file.

Know that a special home.md is searched for if the leaf slug is not a matched file.

Slug means part of url, with / slash to separate. And that sections are like virtual folders which do not appear in the url.

Convenience methods for nodeIs and nodeIsNot are defined in the router.

Section, with a #var  can be made to have a link to its own section home page, off by default.

For instance, imran.wiseowls.life/2025-09/ has month as node and section "with-ai".

Special nodes can be scaffolded via site tsv config. #todo cleanup.

Nodes, sometimes referred to as a page, can have sub pages, now to any depth. And any folder in the node hierarchy can demand a node menu here, by adding an include.php, specifying a number which becomes the position in the bread crumb list. autoSetNode is the router method which sets up required default variables for this.

This generic approach gives a powerful flexibility.

Node menus can have a home link and a flag which says to show only dropdowns in current hierarchy.