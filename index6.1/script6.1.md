const buttons = document.querySelectorAll(".mode-button");
const note = document.querySelector("#mode-note");

buttons.forEach((button) => {
  button.addEventListener("click", () => {
    const mode = button.dataset.mode;
    document.body.classList.toggle("content-box-mode", mode === "content-box");
    document.body.classList.toggle("border-box-mode", mode === "border-box");

    buttons.forEach((item) => {
      const selected = item === button;
      item.classList.toggle("active", selected);
      item.setAttribute("aria-pressed", String(selected));
    });

    note.textContent = mode === "content-box"
      ? "content-box: padding and border are added outside the declared width."
      : "border-box: padding and border are included inside the declared width.";
  });
});

// Start with content-box selected so the experiment is visible immediately.
document.body.classList.add("content-box-mode");
buttons.forEach((button) => {
  button.setAttribute("aria-pressed", String(button.dataset.mode === "content-box"));
});
