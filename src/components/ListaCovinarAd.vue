<template>
    <div class="slecionar2">
        <h1>{{msg}}</h1>
        <h1>Convinar Adornos</h1>
         <select name="language" class="custom-select2" multiple>
         <option value="Vela personajes disney">Vela personajes disney</option>
         <option value="Vela personajes avengers">Vela personajes avengers</option>
        <option value="Vela personajes numeros">Vela personajes numeros</option>
        <option value="Decoracion de nombres con cremas de colores">Decoracion de nombres con cremas de colores</option>
        <option value="Sabores combinados">Sabores combinados</option>
        <option value="Un solo sabor">Un solo sabor</option>
</select>
                   
    </div>
        
</template>

<script>
export default {
    name: 'ListaCovinarAd',
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

document.querySelectorAll(".custom-select2").forEach((selectElement) => {
  new CustomSelect(selectElement);
});
</script>
<style>
  .slecionar2{
    margin-left: 850px;
    margin-top: -150px;
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