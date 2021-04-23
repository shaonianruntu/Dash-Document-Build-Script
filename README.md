# pytorch_docset

The dash documents of pytorch produced by doc2dash, which can be used in [dash](https://kapeli.com/dash) and [zeal](https://zealdocs.org).

I have made some versions and provided those in this github repository,  the file name of the compressed package represents the corresponding pytorch version number.

In addition, you can follow the steps to make your own docset:

## 1st.

download the pytorch source file from [github](https://github.com/pytorch/pytorch) and save it locally.

```
git clone git@github.com:pytorch/pytorch.git
```

## 2nd.

Go to the downloaded pytorch docs directory.

```
cd $PYTORCH/docs
```

>  `$PYTORCH` corresponds to the downloaded file path


## 3rd.

Install the necessary packages as required by the requirements of the `requirements.txt` files in `docs` path.

## 4th.

Call the sphinx package for document processing, and you can select the `make html` command to generate the appropriate HTML document, which will be generated at `./build/html` path.

so run:

```
make html
```

## 5th.

Use `doc2dash` to continue the work of sphinx, generate Dash available document files , use `-n` to specify the generated file name, followed by the source folder path.

First, you should install `doc2dash`:

```
pip install doc2dash
```

Second, use doc2dash to generate docset file from html:

```
doc2dash -n pytorch $PYTORCH/docs/build/html
```

>  `$PYTORCH` corresponds to the downloaded file path

If everything goes well, you can get your docset file now and drag it into dash/zeal to complete the import.

Enjoy it!

--- 

## Reference

[pytorch的zeal文档， Ubuntu](https://www.jianshu.com/p/dfcd79fb635d)


https://xmfbit.github.io/2017/08/26/doc2dash-usage/
