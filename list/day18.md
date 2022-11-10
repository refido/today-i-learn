# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/09 / Week 4

![image](/images/18.png)

We finished our project today despite a very tight deadline, hahahaha, but we did it. Following that, we presented the project's findings to all bootcamp participants.

- What did I learn today?

Since then, I've learned how to use a JSON server to create an API or a database in the meantime. Saya can also send data to APIs using Axios, for example.

```js
const PostForm = () => {
    const { id } = useParams();
    const [description, setDesc] = useState('');

    const handleChangeDesc = event => {
        setDesc(event.target.value)
    }
    const addPost = async () => {
        const a = await axios.patch(`https://placeadvisory-dev.herokuapp.com/posts/${id}`, {description})
        console.log(a)
        setDesc('')
    }

    const handleSubmit = () => {
        addPost()
        alert('kayaknya harus nunggu')
    }


    return (
        <div className="form-wrapper mt-3">
            <h4>Add Description Here</h4>
            <form className="mb-5" onSubmit={handleSubmit}>
                <div className="form">
                    <div className="mb-3">
                        <label className="form-label align-self-center">Description</label>
                        <input type="text" className="form-control" placeholder='change description'
                            required value={description} onChange={handleChangeDesc} />
                    </div>
                </div>
                <div className="button">
                    <button className="btn submit-button px-5" type='submit'>Update</button>
                </div>
            </form>
        </div>
    )
}
```

- What did I do well?

View manipulation in React is similar to displaying or hiding components on the screen. example

```js
const [isShown, setIsShown] = useState(false);


const handleClick = event => {
  setIsShown(current => !current);
}

<div onClick={handleClick} className="comment-button text-primary">
Add comment
</div>
{isShown && <CommentForm />}
```

- What needs to improve?

EVERYTHING, particularly my fundamentals, appears to be lagging far behind the others.
