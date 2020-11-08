---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099440"
---
# <span data-ttu-id="6d8d5-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6d8d5-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="6d8d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8d5-103">Skapar en åtkomst kontroll post.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-103">Creates an access control record.</span></span>

## <span data-ttu-id="6d8d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d8d5-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6d8d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d8d5-105">DESCRIPTION</span></span>
<span data-ttu-id="6d8d5-106">Cmdleten **New-AzureStorSimpleAccessControlRecord** skapar en åtkomst kontroll post.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="6d8d5-107">Du kan använda ett **AccessControlRecord** -objekt för att konfigurera volymer.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="6d8d5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d8d5-108">EXAMPLES</span></span>

### <span data-ttu-id="6d8d5-109">Exempel 1: skapa en Access-Controlaccess kontroll post och vänta tills resultaccess-kontrollen</span><span class="sxs-lookup"><span data-stu-id="6d8d5-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="6d8d5-110">Det här kommandot skapar en åtkomst kontroll post med namnet Acr10 för iSCSI Initiator med namnet Iqn10.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="6d8d5-111">Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="6d8d5-112">Exempel 2: skapa en kontroll recordaccess kontroll för Access-Controlaccess</span><span class="sxs-lookup"><span data-stu-id="6d8d5-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="6d8d5-113">Det här kommandot skapar en åtkomst kontroll post med namnet Acr11 för iSCSI Initiator med namnet Iqn11.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="6d8d5-114">Det här kommandot anger inte parametern *WaitForComplete* , och därför startas uppgiften av kommandot och sedan returneras ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="6d8d5-115">Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="6d8d5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d8d5-116">PARAMETERS</span></span>

### <span data-ttu-id="6d8d5-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="6d8d5-117">-ACRName</span></span>
<span data-ttu-id="6d8d5-118">Anger ett namn för åtkomst kontroll posten.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-118">Specifies a name for the access control record.</span></span>

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

### <span data-ttu-id="6d8d5-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="6d8d5-119">-IQNInitiatorName</span></span>
<span data-ttu-id="6d8d5-120">Anger iSCSI-kvalificerat namn (IQN) för den iSCSI-initierare som denna cmdlet tillhandahåller åtkomst för volymen.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="6d8d5-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6d8d5-121">-Profile</span></span>
<span data-ttu-id="6d8d5-122">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6d8d5-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6d8d5-123">-WaitForComplete</span></span>
<span data-ttu-id="6d8d5-124">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="6d8d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8d5-125">CommonParameters</span></span>
<span data-ttu-id="6d8d5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8d5-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8d5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8d5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d8d5-128">INPUTS</span></span>

### <span data-ttu-id="6d8d5-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="6d8d5-129">None</span></span>

## <span data-ttu-id="6d8d5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d8d5-130">OUTPUTS</span></span>

### <span data-ttu-id="6d8d5-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="6d8d5-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="6d8d5-132">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="6d8d5-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="6d8d5-133">Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d8d5-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="6d8d5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d8d5-134">NOTES</span></span>

## <span data-ttu-id="6d8d5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d8d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="6d8d5-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6d8d5-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6d8d5-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6d8d5-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6d8d5-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6d8d5-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6d8d5-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6d8d5-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


