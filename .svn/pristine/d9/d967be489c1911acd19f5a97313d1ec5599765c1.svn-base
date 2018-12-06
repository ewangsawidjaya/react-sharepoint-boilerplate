import React from 'react';

export default class History extends React.Component {
    constructor(props) {
        super(props);

        this.showHistory = this.showHistory.bind(this);
    }

    showHistory() {
        var options = SP.UI.$create_DialogOptions();
        options.width = this.props.width;
        options.height = this.props.height;
        options.url =  _spPageContextInfo.webAbsoluteUrl + '/_layouts/versions.aspx?list=' + this.props.listId + '&ID=' + this.props.itemId;
        
        SP.UI.ModalDialog.showModalDialog(options);
    }

    render() {
        return (
            <button type="button" className="btn" onClick={this.showHistory}><span className="fa fa-history"></span>Version History</button>
        )
    }
}

History.defaultProps = {
    itemId: null,
    listId: null,
    width: 800,
    height: 600
}