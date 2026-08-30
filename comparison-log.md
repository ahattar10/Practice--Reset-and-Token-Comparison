reset-none.css
1. Headings keep their size hierarchy (<h1> bigger than <h2>) 
2. Paragraphs and headings have margins 
3. Lists have indentation and bullets 
4. Links are underlined 
5. Buttons/inputs have visible borders and padding 

2 Conflicting Defaults:
1. Body has an 8px default margin 
2. Use browser-specific fonts 

reset-broad.css 
1. Heading size hierarchy 
2. Margins 
3. Form control borders 

reset-selective.css 
1. Body default margin 
2. Default form fonts 
3. Inconsistent box sizing 

After css change
1.	Tokens defined in :root (action, accent, surface, text, page, space, radius)
2.	All component rules consume tokens via var(--...)
3.	.theme-alt overrides semantic tokens ONL
4.	Alternate theme card: navy button + amber accent + pale blue background
5.	Default theme card: maroon + gold + white — clearly different
6.	Verification: theme change required editing ONLY token values, zero component rule changes
Finding: All three resets produced nearly identical visuals because component-styles.css loads after and overrides most reset rules. The reset choice matters most for unstyled edge cases (spacing rhythm, heading hierarchy, form boundaries).

