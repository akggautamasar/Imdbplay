const express = require("express");

const app = express();
const PORT = process.env.PORT || 3000;

app.get("/title/:imdbId", (req, res) => {
    const imdbId = req.params.imdbId;

    if (!/^tt\d+$/.test(imdbId)) {
        return res.status(404).send("Invalid IMDb ID");
    }

    res.redirect(`https://player.silverlinehub.org/?imdb_id=${imdbId}`);
});

app.get("/", (req, res) => {
    res.send("IMDbPlay is running.");
});

app.listen(PORT, () => {
    console.log(`Server started on ${PORT}`);
});
