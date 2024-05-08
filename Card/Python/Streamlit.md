


## Why should data scientists use Streamlit? 
[Python Tutorial: Streamlit | DataCamp](https://www.datacamp.com/tutorial/streamlit?_x_tr_hist=true)
- No front-end (html, js, css) experience or knowledge is required.
- You don't need to spend days or months to create a web app, you can create a really beautiful machine learning or data science app in only a few hours or even minutes.
- It is compatible with the majority of Python libraries (e.g. pandas, matplotlib, seaborn, plotly, Keras, PyTorch, SymPy(latex)).
- Less code is needed to create amazing web apps.
- Data caching simplifies and speeds up computation pipelines.

```sh
pipenv install streamlit
pipenv shell
streamlit hello
```

## Google Collab
[Google Colab](https://colab.research.google.com/drive/1Y7OBCpBdSHdldxV9XcQEeupNs4w2cAdX?usp=sharing)
[Create\_streamlit\_app.ipynb - Colab](https://colab.research.google.com/github/mrm8488/shared_colab_notebooks/blob/master/Create_streamlit_app.ipynb#scrollTo=meJ36PefNftd)
[How to Launch Streamlit App from Google Colab Notebook - 🚀 Deployment - Streamlit](https://discuss.streamlit.io/t/how-to-launch-streamlit-app-from-google-colab-notebook/42399/17)
[Create\_streamlit\_app.ipynb - Colab](https://colab.research.google.com/github/mrm8488/shared_colab_notebooks/blob/master/Create_streamlit_app.ipynb)


## Troubleshoot
### 4258 illegal hardware instruction (core dumped) (**UNSOLVED**)
[Illegal instruction - 🎈 Using Streamlit - Streamlit](https://discuss.streamlit.io/t/illegal-instruction/7479)

I just did what i previously failed and yet it still run perfectly fine
- What i did
	- Reinstall streamlit via pipenv within shell in pycharm (not worked)
	- Reinstall pipenv and streamlit within shell in pycharm (not worked)
- Accidentally worked
	- Install streamlit via pipenv in terminal (worked)