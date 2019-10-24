# Angular2 Moment Picker

This project is a port of angular-moment-picker for AngularJS

## Installation

npm install angular2-moment-picker

## Usage

```html
<input [value]="moment?.toString()" (click)="click()">

<angular2-moment-picker 
        [moment]="moment"
        [minview]="'year'"
        [maxview]="'date'"
        [startview]="'month'"
        [onlyupdateatend]="'true'"
        (changed)="changed($event)" #angular2momentpicker></angular2-moment-picker>
<lib-angular2-moment-picker
        [minview]="'year'" [maxview]="'date'" [startview]="'month'" (changed)="changed($event)"
></lib-angular2-moment-picker>
```

```typescript
export class ExampleComponent {

    public moment: moment.Moment;

    @ViewChild('angular2momentpicker', { static: false }) picker;

    constructor() { }

    public click() {
        this.picker.show();
    }

    public changed(event: moment.Moment) {
        this.momentBasic = event;
    }
}
```

## Development

### Build

Run `ng build moment-picker` to build the project.

## Publishing to NPM

`cd dist/moment-picker`
`npm publish`
