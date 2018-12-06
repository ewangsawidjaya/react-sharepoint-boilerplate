import React from 'react';
import StyledContainer from '../../common/styled-container';
import StyledRow from '../../common/styled-row';
import ItemTable from '../../common/item-table';

import cloneDeep from 'lodash/cloneDeep';

export default class ItemTableView extends React.Component {
    constructor(props) {
        super(props);

        this.handleChange = this.handleChange.bind(this);
        this.handleRemove = this.handleRemove.bind(this);

        this.state = {
            items: [],
            types: {
                Title: {type: "Text", label: "Text", visible: true, editable: true, pattern:/Hello World!/g, required: true},
                Description: {type: "Note", label: "Description", visible: true, editable: true, required: false},
                Number: {type: "Number", label: "Number", visible: true, editable: true, required: true},
                Choice: {type: "Choice", label: "Choice", options:[
                    {label:"Red", value:"Red"}, 
                    {label:"Green", value:"Green"}, 
                    {label:"Blue", value:"Blue"}
                ], visible: true, editable: true, required: true},
                Date: {type: "DateTime", label: "Date", maxDate: new Date(), visible: true, editable: true, required: false},
                Currency: {type: "Currency", label: "Currency", visible: true, editable: true, required: true},
                Boolean: {type: "Choice", label: "Boolean", options:[
                    {label: "Yes", value:1}, 
                    {label: "No", value:0}
                ], visible: true, editable: true, required: false},
                UserId: {type: "User", label: "User", visible: true, editable: true, required: true},
                UserMultiId: {type: "UserMulti", label: "UserMulti", visible: true, editable: true, required: true},
                MultiChoice: {type: "MultiChoice", label: "MultiChoice", options:[
                    {label:"Apple", value:"Apple"},
                    {label:"Orange", value:"Orange"},
                    {label:"Banana", value:"Banana"},
                    {label:"Mango", value:"Mango"},
                    {label:"Cantaloupe", value:"Cantaloupe"},
                    {label:"Watermelon", value:"Watermelon"},
                ], visible: true, editable: true, required: true},
                LookupId: {type: "SearchableChoice", label: "Lookup", options:[
                    {label:"Chicken", value:1}, 
                    {label:"Pig", value:2}, 
                    {label:"Cow", value:3}, 
                    {label:"Cat", value:4},
                    {label:"Dog", value:5},
                    {label:"Mouse", value:6},
                    {label:"Hamster", value:7}
                ], visible: true, editable: true, required: true},
            },
            item: {
                ID: null,
                Title: "",
                Description: "",
                Number: 0,
                Choice: "",
                Date: null,
                Currency: 0,
                Boolean: 0,
                UserId: null,
                UserMultiId: [],
                MultiChoice: [],
                LookupId: null,
            }
        }
    }

    handleChange(items) {
        this.setState({items: items});
    }

    handleRemove(item, index) {
        let items = cloneDeep(this.state.items);
            items.splice(index, 1);

        this.setState({items: items});
    }

    render() {
        let disabled = '';
        let addDisabled = '';
        let removeDisabled = '';

        return(
            <div>
                <StyledContainer 
                    className='ItemTableView' 
                    id='ItemTableView'
                    title='Item Table'
                    description={(
                        <p>
                            Below is an example of how to use the ItemTable component.
                        </p>
                    )}
                >
                    <ItemTable 
                        items={this.state.items}
                        typeSchema={this.state.types}
                        itemSchema={this.state.item}
                        onChange={this.handleChange}
                        onRemove={this.handleRemove}
                        disabled={disabled}
                        addDisabled={addDisabled}
                        removeDisabled={removeDisabled}
                        id="item-table"
                    />
                </StyledContainer>
                <StyledContainer
                    title="Usage"
                    className="ImageEditorCode"
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
import ItemTable from '../../common/item-table';

import cloneDeep from 'lodash/cloneDeep';

export default class ItemTableView extends React.Component {
    constructor(props) {
        super(props);

        this.handleChange = this.handleChange.bind(this);
        this.handleRemove = this.handleRemove.bind(this);

        this.state = {
            items: [],
            types: {
                Title: {type: "Text", label: "Text", visible: true, editable: true, pattern:/Hello World!/g, required: true},
                Description: {type: "Note", label: "Description", visible: true, editable: true, required: false},
                Number: {type: "Number", label: "Number", visible: true, editable: true, required: true},
                Choice: {type: "Choice", label: "Choice", options:[
                    {label:"Red", value:"Red"}, 
                    {label:"Green", value:"Green"}, 
                    {label:"Blue", value:"Blue"}
                ], visible: true, editable: true, required: true},
                Date: {type: "DateTime", label: "Date", maxDate: new Date(), visible: true, editable: true, required: false},
                Currency: {type: "Currency", label: "Currency", visible: true, editable: true, required: true},
                Boolean: {type: "Choice", label: "Boolean", options:[
                    {label: "Yes", value:1}, 
                    {label: "No", value:0}
                ], visible: true, editable: true, required: false},
                UserId: {type: "User", label: "User", visible: true, editable: true, required: true},
                UserMultiId: {type: "UserMulti", label: "UserMulti", visible: true, editable: true, required: true},
                MultiChoice: {type: "MultiChoice", label: "MultiChoice", options:[
                    {label:"Apple", value:"Apple"},
                    {label:"Orange", value:"Orange"},
                    {label:"Banana", value:"Banana"},
                    {label:"Mango", value:"Mango"},
                    {label:"Cantaloupe", value:"Cantaloupe"},
                    {label:"Watermelon", value:"Watermelon"},
                ], visible: true, editable: true, required: true},
                LookupId: {type: "SearchableChoice", label: "Lookup", options:[
                    {label:"Chicken", value:1}, 
                    {label:"Pig", value:2}, 
                    {label:"Cow", value:3}, 
                    {label:"Cat", value:4},
                    {label:"Dog", value:5},
                    {label:"Mouse", value:6},
                    {label:"Hamster", value:7}
                ], visible: true, editable: true, required: true},
            },
            item: {
                ID: null,
                Title: "",
                Description: "",
                Number: 0,
                Choice: "",
                Date: null,
                Currency: 0,
                Boolean: 0,
                UserId: null,
                UserMultiId: [],
                MultiChoice: [],
                LookupId: null,
            }
        }
    }

    handleChange(items) {
        this.setState({items: items});
    }

    handleRemove(item, index) {
        let items = cloneDeep(this.state.items);
            items.splice(index, 1);

        this.setState({items: items});
    }

    render() {
        let disabled = '';
        let addDisabled = '';
        let removeDisabled = '';

        return(
            <div>
                <StyledContainer 
                    className='ItemTableView' 
                    id='ItemTableView'
                    title='Item Table'
                >
                    <ItemTable 
                        items={this.state.items}
                        typeSchema={this.state.types}
                        itemSchema={this.state.item}
                        onChange={this.handleChange}
                        onRemove={this.handleRemove}
                        disabled={disabled}
                        addDisabled={addDisabled}
                        removeDisabled={removeDisabled}
                        id="item-table"
                    />
                </StyledContainer>
            </div>
        )
    }
}`