## Superdense coding
Superdense coding bruger simpelt, men elegant, de fundementale principper i kvantemekanikken. Princippet er at to parter, eks. Alice og Bob, deler et par qubits
i bellstate'en. 

<img src="image/bell.png" width=20% height=20%>

Med dette delte par qubits, ønsker Alice ved blot at sende Bob en qubit, at sende to bits klassisk information til Bob. Dette er en klassisk umulig opgave.
Tanken er den, at givet om Alice ønsker at sende 00, 01, 10 eller 11 som den klassiske bitstring til Bob, udfører hun en ud af fire operationer på sin qubit, og sender
den derefter til Bob. 

<img src="image/alice-encode-latex.png" width=60% height=60%>

Efter modtagelsen af Alice's qubit er tricket, at Bob ikke behæver nogen information om den Alice's qubit for at decode beskeden. Han udfører blot CNOT gate, hvor Alice's qubit er control-qubit'en og hans egen er target-qubit'en, herefter udfører han en hadamard gate på Alice's qubit, og måler til sidst begge qubits i den computationelle basis.
I python via IBM's qiskit library, initialiseres den delte bell state på følgende vis;

    # Importer pakker
    from qiskit import QuantumCircuit
    from qiskit import IBMQ, Aer, transpile, assemble
    from qiskit.visualization import plot_histogram
    
    qc = QuantumCircuit(2)
    qc.h(1)
    qc.cx(1, 0)

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/fred465f/Frederiks_Portfolio/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

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

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/fred465f/Frederiks_Portfolio/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
