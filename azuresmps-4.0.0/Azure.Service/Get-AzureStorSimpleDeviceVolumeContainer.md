---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093289"
---
# <span data-ttu-id="0fb36-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0fb36-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="0fb36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fb36-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb36-103">Får volym behållare på en enhet.</span><span class="sxs-lookup"><span data-stu-id="0fb36-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="0fb36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fb36-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0fb36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fb36-105">DESCRIPTION</span></span>
<span data-ttu-id="0fb36-106">Cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** hämtar en lista med volym behållare på en enhet eller volym behållare som har det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="0fb36-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="0fb36-107">Det returnerade objektet innehåller följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="0fb36-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="0fb36-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="0fb36-108">**BandwidthRate**</span></span>
- <span data-ttu-id="0fb36-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="0fb36-109">**EncryptionKey**</span></span>
- <span data-ttu-id="0fb36-110">**Instans**</span><span class="sxs-lookup"><span data-stu-id="0fb36-110">**InstanceId**</span></span>
- <span data-ttu-id="0fb36-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="0fb36-111">**IsDefault**</span></span>
- <span data-ttu-id="0fb36-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="0fb36-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="0fb36-113">**Namn**</span><span class="sxs-lookup"><span data-stu-id="0fb36-113">**Name**</span></span>
- <span data-ttu-id="0fb36-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="0fb36-114">**OperationInProgress**</span></span>
- <span data-ttu-id="0fb36-115">**Höra**</span><span class="sxs-lookup"><span data-stu-id="0fb36-115">**Owned**</span></span>
- <span data-ttu-id="0fb36-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="0fb36-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="0fb36-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="0fb36-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="0fb36-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="0fb36-118">**VolumeCount**</span></span>

## <span data-ttu-id="0fb36-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fb36-119">EXAMPLES</span></span>

### <span data-ttu-id="0fb36-120">Exempel 1: Hämta alla behållare på en enhet</span><span class="sxs-lookup"><span data-stu-id="0fb36-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="0fb36-121">Det här kommandot får en lista med volym behållarna på enheten som heter 8600-Bravo 001.</span><span class="sxs-lookup"><span data-stu-id="0fb36-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="0fb36-122">Exempel 2: Hämta en behållare genom att använda namnet</span><span class="sxs-lookup"><span data-stu-id="0fb36-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="0fb36-123">Det här kommandot får volymen som heter Container08 på enheten Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="0fb36-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="0fb36-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fb36-124">PARAMETERS</span></span>

### <span data-ttu-id="0fb36-125">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="0fb36-125">-DeviceName</span></span>
<span data-ttu-id="0fb36-126">Anger namnet på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="0fb36-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="0fb36-127">Denna cmdlet får volym behållare från den enhet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0fb36-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb36-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="0fb36-128">-Profile</span></span>
<span data-ttu-id="0fb36-129">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="0fb36-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0fb36-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="0fb36-130">-VolumeContainerName</span></span>
<span data-ttu-id="0fb36-131">Anger namnet på den volym behållare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="0fb36-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fb36-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb36-132">CommonParameters</span></span>
<span data-ttu-id="0fb36-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fb36-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb36-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb36-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb36-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fb36-135">INPUTS</span></span>

### <span data-ttu-id="0fb36-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="0fb36-136">None</span></span>

## <span data-ttu-id="0fb36-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fb36-137">OUTPUTS</span></span>

### <span data-ttu-id="0fb36-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="0fb36-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="0fb36-139">Denna cmdlet returnerar ett **DataContainer** -objekt om du anger parametern *VolumeContainerName* .</span><span class="sxs-lookup"><span data-stu-id="0fb36-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="0fb36-140">Om du inte anger den parametern returnerar denna cmdlet ett **ilist \<DataContainer\>** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0fb36-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="0fb36-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fb36-141">NOTES</span></span>

## <span data-ttu-id="0fb36-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fb36-142">RELATED LINKS</span></span>

[<span data-ttu-id="0fb36-143">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0fb36-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="0fb36-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="0fb36-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


