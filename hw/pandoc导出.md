```zsh
pandoc --citeproc --number-sections \
--csl APA7.csl \
--bibliography /Users/lintianjian/Downloads/基因编辑技术与肿瘤学/基因编辑技术与 肿瘤学.bib -M reference-section-title="参考文献" \
-M link-citations=true --reference-doc custom-reference.docx /Users/lintianjian/Documents/"Obsidian Vault"/hw/基因编辑技术及在肿瘤学研究中的发展.md -o 基因编辑 技术在肿瘤学研究中的发展_1.docx
```
