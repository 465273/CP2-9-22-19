# CP2-9-22-19

import React, { Component } from "react";
import ReactDOM from "react-dom";

import "./styles.css";

var pages = {
  start: {
    text: "Welcome, traveler! How would you like to get to your destination?",
    leftLabel: "Train",
    rightLabel: "Ship",
    leftPage: "Uber",
    rightPage: "FortniteBus"
  },
  Uber: {
    text: "Uber here, am outside",
    leftLabel: "where",
    rightLabel: "where",
    leftPage: "where",
    rightPage: "where"
  },
  FortniteBus: {
    text: "Welcome to Minecraft",
    leftLabel: "MinecraftMoment",
    rightLabel: "MinecraftMoment",
    leftPage: "nice",
    rightPage: "MinecraftMoment"
  },
  Ship: {
    text: "Your boat sank",
    leftLabel: "aight",
    rightLabel: "cool",
    leftPage: "k",
    rightPage: "nice"
  },
  Train: {
    text: "The train leaves at 4:20",
    leftLabel: "nice",
    rightLabel: "nice",
    leftPage: "nice",
    rightPage: "nice"
  },
  onthetrain: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  where: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  nice: {
    text: "is it tho",
    leftLabel: "yea",
    rightLabel: "yeah",
    leftPage: "yeaFuckNo",
    rightPage: "ya"
  },
  yea: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  k: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  cool: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  aight: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  yeaFuckNo: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  ya: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  yeah: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  },
  MinecraftMoment: {
    text: "train time",
    leftLabel: "train time",
    rightLabel: "train time",
    leftPage: "train time",
    rightPage: "train time"
  }
};
class App extends Component {
  constructor(props) {
    super(props);
    this.state = {
      page: "start"
    };
  }

  goToPage(pageName) {
    this.setState({
      page: pageName
    });
  }

  render() {
    var pageData = pages[this.state.page];

    return (
      <div className="App">
        <p>{pageData.text}</p>
        <button onClick={() => this.goToPage(pageData.rightLabel)}>
          {pageData.rightLabel}
        </button>
        <button onClick={() => this.goToPage(pageData.leftLabel)}>
          {pageData.leftLabel}
        </button>
        <button onClick={() => this.goToPage(pageData.leftPage)}>
          {pageData.leftPage}
        </button>
        <button onClick={() => this.goToPage(pageData.rightPage)}>
          {pageData.rightPage}
        </button>

        <a href="https://images3.memedroid.com/images/UPLOADED337/5d0f8e5823b74.jpeg" />
      </div>
    );
  }
}
const rootElement = document.getElementById("root");
ReactDOM.render(<App />, rootElement);
