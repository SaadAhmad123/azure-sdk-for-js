## API Report File for "@azure/communication-rooms"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { CommonClientOptions } from '@azure/core-client';
import { CommunicationIdentifier } from '@azure/communication-common';
import { CommunicationUserIdentifier } from '@azure/communication-common';
import { KeyCredential } from '@azure/core-auth';
import { OperationOptions } from '@azure/core-client';
import { TokenCredential } from '@azure/core-auth';

// @public
export type AddParticipantsOptions = OperationOptions;

// @public
export interface CreateRoomOptions extends OperationOptions {
    participants?: RoomParticipant[];
    roomJoinPolicy?: RoomJoinPolicy;
    validFrom?: Date;
    validUntil?: Date;
}

// @public
export type DeleteRoomOptions = OperationOptions;

// @public
export type GetParticipantsOptions = OperationOptions;

// @public
export type GetRoomOptions = OperationOptions;

// @public
export type RemoveParticipantsOptions = OperationOptions;

// @public
export type Role = "Presenter" | "Attendee" | "Consumer";

// @public
export interface Room {
    createdOn: Date;
    id: string;
    joinPolicy: RoomJoinPolicy;
    participants: RoomParticipant[];
    validFrom: Date;
    validUntil: Date;
}

// @public
export type RoomJoinPolicy = "InviteOnly" | "CommunicationServiceUsers";

// @public
export interface RoomParticipant {
    id: CommunicationIdentifier;
    role?: Role;
}

// @public
export class RoomsClient {
    constructor(connectionString: string, options?: RoomsClientOptions);
    constructor(endpoint: string, credential: KeyCredential, options?: RoomsClientOptions);
    constructor(endpoint: string, credential: TokenCredential, options?: RoomsClientOptions);
    addParticipants(roomId: string, participants: RoomParticipant[], options?: AddParticipantsOptions): Promise<void>;
    createRoom(options?: CreateRoomOptions): Promise<Room>;
    deleteRoom(roomId: string, options?: DeleteRoomOptions): Promise<void>;
    getParticipants(roomId: string, options?: GetParticipantsOptions): Promise<RoomParticipant[]>;
    getRoom(roomId: string, options?: GetRoomOptions): Promise<Room>;
    removeParticipants(roomId: string, participants: CommunicationUserIdentifier[], options?: RemoveParticipantsOptions): Promise<void>;
    updateParticipants(roomId: string, participants: RoomParticipant[], options?: UpdateParticipantsOptions): Promise<void>;
    updateRoom(roomId: string, options?: UpdateRoomOptions): Promise<Room>;
}

// @public
export interface RoomsClientOptions extends CommonClientOptions {
}

// @public
export type UpdateParticipantsOptions = OperationOptions;

// @public
export interface UpdateRoomOptions extends OperationOptions {
    participants?: RoomParticipant[];
    roomJoinPolicy?: RoomJoinPolicy;
    validFrom?: Date;
    validUntil?: Date;
}

// (No @packageDocumentation comment for this package)

```
