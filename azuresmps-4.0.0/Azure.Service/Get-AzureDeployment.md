---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099585"
---
# <span data-ttu-id="85e56-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="85e56-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="85e56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85e56-102">SYNOPSIS</span></span>
<span data-ttu-id="85e56-103">Hämtar information om en distribution.</span><span class="sxs-lookup"><span data-stu-id="85e56-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="85e56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85e56-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="85e56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85e56-105">DESCRIPTION</span></span>
<span data-ttu-id="85e56-106">Cmdleten **Get-AzureDeployment** hämtar information om en Azure-distribution.</span><span class="sxs-lookup"><span data-stu-id="85e56-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="85e56-107">Ange namnet på Azure-tjänsten och distributionen.</span><span class="sxs-lookup"><span data-stu-id="85e56-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="85e56-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85e56-108">EXAMPLES</span></span>

### <span data-ttu-id="85e56-109">Exempel 1: få information om en produktions distribution</span><span class="sxs-lookup"><span data-stu-id="85e56-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="85e56-110">Det här kommandot returnerar information om distributionen för tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="85e56-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="85e56-111">Det här kommandot anger inte en plats.</span><span class="sxs-lookup"><span data-stu-id="85e56-111">This command does not specify a slot.</span></span>
<span data-ttu-id="85e56-112">Därför använder kommandot standardvärdet för produktion.</span><span class="sxs-lookup"><span data-stu-id="85e56-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="85e56-113">Exempel 2: få information om en implementerings distribution</span><span class="sxs-lookup"><span data-stu-id="85e56-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="85e56-114">Det här kommandot returnerar detaljerna för mellanlagrings distributionen av ContosoService.</span><span class="sxs-lookup"><span data-stu-id="85e56-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="85e56-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85e56-115">PARAMETERS</span></span>

### <span data-ttu-id="85e56-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="85e56-116">-InformationAction</span></span>
<span data-ttu-id="85e56-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="85e56-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="85e56-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="85e56-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85e56-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="85e56-119">Continue</span></span>
- <span data-ttu-id="85e56-120">Över</span><span class="sxs-lookup"><span data-stu-id="85e56-120">Ignore</span></span>
- <span data-ttu-id="85e56-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="85e56-121">Inquire</span></span>
- <span data-ttu-id="85e56-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="85e56-122">SilentlyContinue</span></span>
- <span data-ttu-id="85e56-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="85e56-123">Stop</span></span>
- <span data-ttu-id="85e56-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="85e56-124">Suspend</span></span>

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

### <span data-ttu-id="85e56-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="85e56-125">-InformationVariable</span></span>
<span data-ttu-id="85e56-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="85e56-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="85e56-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="85e56-127">-Profile</span></span>
<span data-ttu-id="85e56-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="85e56-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85e56-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="85e56-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85e56-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="85e56-130">-ServiceName</span></span>
<span data-ttu-id="85e56-131">Anger namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="85e56-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="85e56-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="85e56-132">-Slot</span></span>
<span data-ttu-id="85e56-133">Anger distributionens miljö.</span><span class="sxs-lookup"><span data-stu-id="85e56-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="85e56-134">Giltiga värden är: för produktion eller produktion.</span><span class="sxs-lookup"><span data-stu-id="85e56-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="85e56-135">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="85e56-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e56-136">CommonParameters</span></span>
<span data-ttu-id="85e56-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e56-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e56-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e56-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85e56-139">INPUTS</span></span>

## <span data-ttu-id="85e56-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85e56-140">OUTPUTS</span></span>

## <span data-ttu-id="85e56-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85e56-141">NOTES</span></span>

## <span data-ttu-id="85e56-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85e56-142">RELATED LINKS</span></span>

[<span data-ttu-id="85e56-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="85e56-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="85e56-144">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="85e56-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="85e56-145">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="85e56-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="85e56-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="85e56-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="85e56-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="85e56-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


