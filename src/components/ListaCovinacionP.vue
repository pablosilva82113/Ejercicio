<template>
    <div class="slecionar">
        <h1>{{msg}}</h1>
        <h1>Convinar sabores</h1>
         <select name="language" class="custom-select" multiple>
         <option value="Pasteles de Merengue">Pasteles de Merengue</option>
         <option value="Dacquoise">Dacquoise</option>
        <option value="Angel food">Angel food</option>
        <option value="Chiffon">Chiffon</option>
        <option value="Pastel de zanahoria">Pastel de zanahoria</option>
        <option value="Devil’s food">Devil’s food</option>
</select>
                   
    </div>
        
</template>

<script>
export default {
    name: 'ListaCovinacionP',
    props: {
        msg: String
    }
  
}
 class CustomSelect {
  constructor(originalSelect) {
    this.originalSelect = originalSelect;
    this.customSelect = document.createElement("div");
    this.customSelect.classList.add("select");

    this.originalSelect.querySelectorAll("option").forEach((optionElement) => {
      const itemElement = document.createElement("div");

      itemElement.classList.add("select__item");
      itemElement.textContent = optionElement.textContent;
      this.customSelect.appendChild(itemElement);

      if (optionElement.selected) {
        this._select(itemElement);
      }

      itemElement.addEventListener("click", () => {
        if (
          this.originalSelect.multiple &&
          itemElement.classList.contains("select__item--selected")
        ) {
          this._deselect(itemElement);
        } else {
          this._select(itemElement);
        }
      });
    });

    this.originalSelect.insertAdjacentElement("afterend", this.customSelect);
    this.originalSelect.style.display = "none";
  }

  _select(itemElement) {
    const index = Array.from(this.customSelect.children).indexOf(itemElement);

    if (!this.originalSelect.multiple) {
      this.customSelect.querySelectorAll(".select__item").forEach((el) => {
        el.classList.remove("select__item--selected");
      });
    }

    this.originalSelect.querySelectorAll("option")[index].selected = true;
    itemElement.classList.add("select__item--selected");
  }

  _deselect(itemElement) {
    const index = Array.from(this.customSelect.children).indexOf(itemElement);

    this.originalSelect.querySelectorAll("option")[index].selected = false;
    itemElement.classList.remove("select__item--selected");
  }
}

document.querySelectorAll(".custom-select").forEach((selectElement) => {
  new CustomSelect(selectElement);
});
</script>
<style>
.slecionar{
    margin-right: 450px;
}
.select {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  max-width: 300px;
  gap: 1px;
}

.select__item {
  padding: 10px;
  cursor: pointer;
  font-family: "Heebo", sans-serif;
  text-align: center;
  border-radius: 3px;
  background: #eeeeee;
  transition: background 0.1s;
}

.select__item--selected {
  background: #009578;
  color: #ffffff;
}

</style>