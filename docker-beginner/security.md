#In this step we will learn 

* Running the application inside the container as a User

```
FROM ubuntu

RUN groupadd -r prospa && useradd -r -g prospa prospa

USER prospa

ENTRYPOINT ["sleep"]
CMD ["1000"]
```