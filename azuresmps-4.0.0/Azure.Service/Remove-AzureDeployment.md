---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099395"
---
# <span data-ttu-id="80b6b-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="80b6b-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="80b6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="80b6b-103">Tar bort en distribution av en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="80b6b-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="80b6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80b6b-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="80b6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="80b6b-106">Cmdleten **Remove-AzureDeployment** tar bort en distribution av en Azure Cloud-tjänst.</span><span class="sxs-lookup"><span data-stu-id="80b6b-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="80b6b-107">Om du vill ta bort en distribution ska du först stoppa den.</span><span class="sxs-lookup"><span data-stu-id="80b6b-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="80b6b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80b6b-108">EXAMPLES</span></span>

### <span data-ttu-id="80b6b-109">Exempel 1: ta bort en distribution</span><span class="sxs-lookup"><span data-stu-id="80b6b-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="80b6b-110">Det här kommandot tar bort distributionen av Azure-tjänsten med namnet ContosoService.</span><span class="sxs-lookup"><span data-stu-id="80b6b-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="80b6b-111">Eftersom det här kommandot inte anger någon plats tas tjänsten bort från produktions miljön.</span><span class="sxs-lookup"><span data-stu-id="80b6b-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="80b6b-112">Exempel 2: ta bort en distribution och virtuella hård diskar</span><span class="sxs-lookup"><span data-stu-id="80b6b-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="80b6b-113">Det här kommandot tar bort distributionen av tjänsten som heter ContosoService från produktions miljön.</span><span class="sxs-lookup"><span data-stu-id="80b6b-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="80b6b-114">Kommandot tar också bort underliggande virtuella hård diskar.</span><span class="sxs-lookup"><span data-stu-id="80b6b-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="80b6b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80b6b-115">PARAMETERS</span></span>

### <span data-ttu-id="80b6b-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="80b6b-116">-DeleteVHD</span></span>
<span data-ttu-id="80b6b-117">Anger att denna cmdlet tar bort distributionen och virtuella hård diskar (VHD: er) från Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="80b6b-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b6b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="80b6b-118">-Force</span></span>
<span data-ttu-id="80b6b-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="80b6b-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b6b-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80b6b-120">-InformationAction</span></span>
<span data-ttu-id="80b6b-121">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="80b6b-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80b6b-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="80b6b-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80b6b-123">Vidare</span><span class="sxs-lookup"><span data-stu-id="80b6b-123">Continue</span></span>
- <span data-ttu-id="80b6b-124">Över</span><span class="sxs-lookup"><span data-stu-id="80b6b-124">Ignore</span></span>
- <span data-ttu-id="80b6b-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="80b6b-125">Inquire</span></span>
- <span data-ttu-id="80b6b-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80b6b-126">SilentlyContinue</span></span>
- <span data-ttu-id="80b6b-127">Stanna</span><span class="sxs-lookup"><span data-stu-id="80b6b-127">Stop</span></span>
- <span data-ttu-id="80b6b-128">Avbryt</span><span class="sxs-lookup"><span data-stu-id="80b6b-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b6b-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80b6b-129">-InformationVariable</span></span>
<span data-ttu-id="80b6b-130">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="80b6b-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b6b-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="80b6b-131">-Profile</span></span>
<span data-ttu-id="80b6b-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="80b6b-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80b6b-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="80b6b-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80b6b-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="80b6b-134">-ServiceName</span></span>
<span data-ttu-id="80b6b-135">Anger namnet på den tjänst där denna cmdlet tar bort en distribution.</span><span class="sxs-lookup"><span data-stu-id="80b6b-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b6b-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="80b6b-136">-Slot</span></span>
<span data-ttu-id="80b6b-137">Anger distributions miljön som den här cmdleten tar bort distributionen från.</span><span class="sxs-lookup"><span data-stu-id="80b6b-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="80b6b-138">Giltiga värden är: för produktion och produktion.</span><span class="sxs-lookup"><span data-stu-id="80b6b-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="80b6b-139">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="80b6b-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b6b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b6b-140">CommonParameters</span></span>
<span data-ttu-id="80b6b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b6b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b6b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b6b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b6b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80b6b-143">INPUTS</span></span>

## <span data-ttu-id="80b6b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80b6b-144">OUTPUTS</span></span>

### <span data-ttu-id="80b6b-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="80b6b-145">ManagementOperationContext</span></span>

## <span data-ttu-id="80b6b-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80b6b-146">NOTES</span></span>

## <span data-ttu-id="80b6b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80b6b-147">RELATED LINKS</span></span>

[<span data-ttu-id="80b6b-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="80b6b-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="80b6b-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="80b6b-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="80b6b-150">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="80b6b-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="80b6b-151">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="80b6b-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="80b6b-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="80b6b-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


