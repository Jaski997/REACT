# przepisy-react
> 

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info
Strona stworzona na architekturze javascript i react, ktorej zadaniem jest wyszukiwanie przepisów do dań, po wpisaniu ich nazwy

## Screenshots
![Example screenshot](./img/screenshot.png)

## Technologies
* Axios - version 6.14.12
* ES 7 - version 2.8.-
* Tech 3 - version 3.0

## Setup
npm install axios


## Przyklady kodu
Pobranie Przepisu
`const getRecipeInfo = async () => {
    var result = await Axios.get(url);
    setrecipes(result.data.hits);
    console.log(result.data.hits);
  };

  const onSubmit = (e) => {
    e.preventDefault();
    getRecipeInfo();
  };
`
Eksportowanie przepisów wraz z obrazkiem
`
export default function RecipeTile({ recipe }) {
  return (
    recipe["recipe"]["image"].match(/\.(jpeg|jpg|gif|png)$/) != null && (
      <div
        className="recipeTile"
        onClick={() => window.open(recipe["recipe"]["url"])}
      >
        <img className="recipeTile__img" src={recipe["recipe"]["image"]} />
        <p className="recipeTile__name" key={uuidv4()}>
          {recipe["recipe"]["label"]}
        </p>
      </div>
`

## Features
List of features ready and TODOs for future development
* Odnajdywanie Przepisów
* Obrazki pomagaja uzytkownikowi w wyborze przepisu

To-do list:
* Poprawić Front-end , strona wyglada na bardzo podstawowa strone
* Dodać wyszukiwanie nie tylko po nazwie, ale i po skladnikach

## Status
Zakończony

## Inspiration
Projekt oparty na : https://www.youtube.com/watch?v=tPqnKDBaMLQ&ab_channel=SanskarTiwari
https://www.youtube.com/watch?v=T3Px88x_PsA&ab_channel=BenAwad
https://www.youtube.com/watch?v=d1vT4kkTCaw&ab_channel=CodeAndCreate

## Contact
Created by [@flynerdpl](https://www.flynerd.pl/) - feel free to contact me!
