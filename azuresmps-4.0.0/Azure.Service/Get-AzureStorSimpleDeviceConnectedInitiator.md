---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099521"
---
# <span data-ttu-id="f6960-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="f6960-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="f6960-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6960-102">SYNOPSIS</span></span>
<span data-ttu-id="f6960-103">Tar emot iSCSI-anslutningar för en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="f6960-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="f6960-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6960-104">SYNTAX</span></span>

### <span data-ttu-id="f6960-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="f6960-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6960-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="f6960-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6960-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6960-107">DESCRIPTION</span></span>
<span data-ttu-id="f6960-108">Cmdleten **Get-AzureStorSimpleDeviceConnectedInitiator** hämtar en lista över tillgängliga iSCSI-anslutningar för en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="f6960-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="f6960-109">De iSCSI-Connection-objekt som denna cmdlet returnerar innehåller följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="f6960-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="f6960-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="f6960-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="f6960-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="f6960-111">**AcrName**</span></span>
- <span data-ttu-id="f6960-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="f6960-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="f6960-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="f6960-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="f6960-114">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="f6960-114">**Interfaces**</span></span>
- <span data-ttu-id="f6960-115">**IQN**</span><span class="sxs-lookup"><span data-stu-id="f6960-115">**Iqn**</span></span>
- <span data-ttu-id="f6960-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="f6960-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="f6960-117">Denna cmdlet får anslutnings objekt endast om iSCSI-anslutningar är aktiverade för enheten.</span><span class="sxs-lookup"><span data-stu-id="f6960-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="f6960-118">Standardinställningen är att anslutningar är avstängda.</span><span class="sxs-lookup"><span data-stu-id="f6960-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="f6960-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6960-119">EXAMPLES</span></span>

### <span data-ttu-id="f6960-120">Exempel 1: Hämta alla anslutningar för en enhet</span><span class="sxs-lookup"><span data-stu-id="f6960-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="f6960-121">Det här kommandot får alla iSCSI-anslutningar för enheten med namnet Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f6960-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f6960-122">Det här kommandot returnerar endast anslutningar om anslutningar är aktiverade för enheten.</span><span class="sxs-lookup"><span data-stu-id="f6960-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="f6960-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6960-123">PARAMETERS</span></span>

### <span data-ttu-id="f6960-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f6960-124">-DeviceId</span></span>
<span data-ttu-id="f6960-125">Anger instans-ID för den StorSimple-enhet som iSCSI-initierare ska tilldelas från.</span><span class="sxs-lookup"><span data-stu-id="f6960-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6960-126">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="f6960-126">-DeviceName</span></span>
<span data-ttu-id="f6960-127">Anger namnet på den StorSimple-enhet som iSCSI-initierare ska tilldelas från.</span><span class="sxs-lookup"><span data-stu-id="f6960-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6960-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6960-128">-Profile</span></span>
<span data-ttu-id="f6960-129">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="f6960-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f6960-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6960-130">CommonParameters</span></span>
<span data-ttu-id="f6960-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6960-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6960-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6960-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6960-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6960-133">INPUTS</span></span>

### <span data-ttu-id="f6960-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6960-134">None</span></span>

## <span data-ttu-id="f6960-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6960-135">OUTPUTS</span></span>

### <span data-ttu-id="f6960-136">Förteckning\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="f6960-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="f6960-137">Denna cmdlet returnerar ett iSCSI-anslutningsobjektet som innehåller följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="f6960-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="f6960-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="f6960-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="f6960-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="f6960-139">**AcrName**</span></span>
- <span data-ttu-id="f6960-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="f6960-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="f6960-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="f6960-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="f6960-142">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="f6960-142">**Interfaces**</span></span>
- <span data-ttu-id="f6960-143">**IQN**</span><span class="sxs-lookup"><span data-stu-id="f6960-143">**Iqn**</span></span>
- <span data-ttu-id="f6960-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="f6960-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="f6960-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6960-145">NOTES</span></span>

## <span data-ttu-id="f6960-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6960-146">RELATED LINKS</span></span>

[<span data-ttu-id="f6960-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="f6960-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


