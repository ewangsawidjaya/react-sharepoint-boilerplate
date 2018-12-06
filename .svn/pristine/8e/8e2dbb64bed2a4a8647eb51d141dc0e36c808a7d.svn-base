import React from 'react';
import StyledContainer from '../../common/styled-container';
import StyledRow from '../../common/styled-row';
import FilterTable from '../../common/filter-table';

export default class FilterTableView extends React.Component {
    constructor(props) {
        super(props);

        this.state = {
            items: [
                {ID: "1", Title: "Item 1", Color: "Red", Fruit: "Apple, Tomato", Price:"$0.75", Expiry: "12/17/2018", Ranking: "1"},
                {ID: "2", Title: "Item 2", Color: "Orange", Fruit: "Orange, Mango", Price:"$1.25", Expiry: "12/02/2018", Ranking: "3"},
                {ID: "3", Title: "Item 3", Color: "Red", Fruit: "Raspberry, Tomato", Price:"$1.55", Expiry: "11/28/2018", Ranking: "4"},
                {ID: "4", Title: "Item 4", Color: "Yellow", Fruit: "Banana", Price:"$1.25", Expiry: "11/07/2018", Ranking: "2"},
            ]
        }
    }

    render() {
        return(
            <div>
                <StyledContainer 
                    className='FilterTableView' 
                    id='FilterTableView'
                    title='Filter Table'
                    description={(
                        <p>
                            Below is an example of how to use the Filter Table component.
                        </p>
                    )}
                >
                    <FilterTable
                        items={this.state.items}
                        className="item-search"
                    />
                </StyledContainer>
                <StyledContainer
                    title="Usage"
                    className="FilterTableCode"
                >
                    <pre>{code}</pre>
                </StyledContainer>
            </div>
        )
    }
}

const code =
`import React from 'react';
import StyledContainer from '../../common/styled-container';
import StyledRow from '../../common/styled-row';
import FilterTable from '../../common/filter-table';

export default class FilterTableView extends React.Component {
    constructor(props) {
        super(props);

        this.state = {
            items: [
                {ID: "1", Title: "Item 1", 
                    Color: "Red", Fruit: "Apple, Tomato", Price:"$0.75", Expiry: "12/17/2018", Ranking: "1"},
                {ID: "2", Title: "Item 2", 
                    Color: "Orange", Fruit: "Orange, Mango", Price:"$1.25", Expiry: "12/02/2018", Ranking: "3"},
                {ID: "3", Title: "Item 3", 
                    Color: "Red", Fruit: "Raspberry, Tomato", Price:"$1.55", Expiry: "11/28/2018", Ranking: "4"},
                {ID: "4", Title: "Item 4", 
                    Color: "Yellow", Fruit: "Banana", Price:"$1.25", Expiry: "11/07/2018", Ranking: "2"},
            ]
        }
    }

    render() {
        return(
            <div>
                <StyledContainer 
                    className='FilterTableView' 
                    id='FilterTableView'
                    title='Search'
                >
                    <FilterTable
                        items={this.state.items}
                        className="item-search"
                    />
                </StyledContainer>
            </div>
        )
    }
}`;