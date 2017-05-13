## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/brianrabbott/brianrabbott.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text
Here is some SAGE math code, which _actually_ works.
`
# 16.6 problem 3 - the hard way
x,y,z = var('x,y,z')
u,v = var('u,v')
print("we will use u=phi, and v=theta")

# first we deal with our surface S parametrization (r) and the differential
# define parametrization vector
r = vector([sin(u)*cos(v), sin(u)*sin(v), cos(u)])
print("r:")
show(r)

# find partials
r_u = diff(r,u)
print('r_phi:')
show(r_u)

r_v = diff(r,v)
print('r_theta:')
show(r_v)

# find cross product
crossprod = r_u.cross_product(r_v)
print('r_u cross r_v:')
show(crossprod)

# find magnitude of cross product
mag = crossprod.norm()
print("magnitude of cross product")
show(mag)

# define function to be integrated
f(x,y,z) = x^2

# get components of our vector
rx = r[0]
ry = r[1]
rz = r[2]

# evaluate f(r(u,v))
fr = f(rx,ry,rz)
print("f(r(u,v)):")
show(fr)

# define function to integrate
f_final = fr * mag

# integrate our function over our surface S
fv = integrate(f_final,v,0,2*pi)
print("we do 'v' as our inner integral")
show(fv)
print("then the 'u' as our outer integral")
fu = integrate(fv, u, 0, pi)
show(fu)
`

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/brianrabbott/brianrabbott.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
