---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099088"
---
# <span data-ttu-id="7757e-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7757e-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="7757e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7757e-102">SYNOPSIS</span></span>
<span data-ttu-id="7757e-103">Uppdaterar IQN för en åtkomst kontroll post.</span><span class="sxs-lookup"><span data-stu-id="7757e-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="7757e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7757e-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7757e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7757e-105">DESCRIPTION</span></span>
<span data-ttu-id="7757e-106">Cmdleten **set-AzureStorSimpleAccessControlRecord** uppdaterar iSCSI-kvalificerat namn (IQN) för en befintlig åtkomst kontroll post.</span><span class="sxs-lookup"><span data-stu-id="7757e-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="7757e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7757e-107">EXAMPLES</span></span>

### <span data-ttu-id="7757e-108">Exempel 1: uppdatera en åtkomst kontroll post</span><span class="sxs-lookup"><span data-stu-id="7757e-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="7757e-109">Det här kommandot uppdaterar åtkomst kontroll posten med namnet Acr10 för iSCSI Initiator med namnet IqnUpdated.</span><span class="sxs-lookup"><span data-stu-id="7757e-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="7757e-110">Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7757e-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="7757e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7757e-111">PARAMETERS</span></span>

### <span data-ttu-id="7757e-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="7757e-112">-ACRName</span></span>
<span data-ttu-id="7757e-113">Anger ett namn på den åtkomst kontroll posten som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="7757e-113">Specifies a name of the access control record to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7757e-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="7757e-114">-IQNInitiatorName</span></span>
<span data-ttu-id="7757e-115">Anger IQN för iSCSI Initiator som denna cmdlet tillhandahåller åtkomst för volymen.</span><span class="sxs-lookup"><span data-stu-id="7757e-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7757e-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="7757e-116">-NewName</span></span>
<span data-ttu-id="7757e-117">Anger ett nytt namn på åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="7757e-117">Specifies a new name for access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7757e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="7757e-118">-Profile</span></span>
<span data-ttu-id="7757e-119">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="7757e-119">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7757e-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="7757e-120">-WaitForComplete</span></span>
<span data-ttu-id="7757e-121">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="7757e-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7757e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7757e-122">CommonParameters</span></span>
<span data-ttu-id="7757e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7757e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7757e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7757e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7757e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7757e-125">INPUTS</span></span>

### <span data-ttu-id="7757e-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="7757e-126">None</span></span>

## <span data-ttu-id="7757e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7757e-127">OUTPUTS</span></span>

### <span data-ttu-id="7757e-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="7757e-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="7757e-129">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="7757e-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="7757e-130">Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7757e-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="7757e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7757e-131">NOTES</span></span>

## <span data-ttu-id="7757e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7757e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7757e-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7757e-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="7757e-134">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7757e-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="7757e-135">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="7757e-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)


