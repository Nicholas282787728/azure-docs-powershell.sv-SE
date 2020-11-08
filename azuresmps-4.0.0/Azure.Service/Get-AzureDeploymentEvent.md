---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093376"
---
# <span data-ttu-id="c198b-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="c198b-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="c198b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c198b-102">SYNOPSIS</span></span>
<span data-ttu-id="c198b-103">Hämtar information om händelser som Azure initierar som påverkar virtuella datorer och moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="c198b-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="c198b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c198b-104">SYNTAX</span></span>

### <span data-ttu-id="c198b-105">GetDeploymentEventBySlot (standard)</span><span class="sxs-lookup"><span data-stu-id="c198b-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c198b-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="c198b-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c198b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c198b-107">DESCRIPTION</span></span>
<span data-ttu-id="c198b-108">Cmdleten **Get-AzureDeploymentEvent** hämtar information om händelser som Azure initierar som påverkar virtuella datorer och moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="c198b-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="c198b-109">Dessa händelser inkluderar planerade underhålls händelser.</span><span class="sxs-lookup"><span data-stu-id="c198b-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="c198b-110">Denna cmdlet returnerar en lista över händelser som identifierar den roll instans eller virtuell dator som påverkas, anledningen till effekten och start tiden för händelsen.</span><span class="sxs-lookup"><span data-stu-id="c198b-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="c198b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c198b-111">EXAMPLES</span></span>

### <span data-ttu-id="c198b-112">9.1</span><span class="sxs-lookup"><span data-stu-id="c198b-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="c198b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c198b-113">PARAMETERS</span></span>

### <span data-ttu-id="c198b-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c198b-114">-DeploymentName</span></span>
<span data-ttu-id="c198b-115">Anger namnet på den distribution för vilken denna cmdlet får händelser.</span><span class="sxs-lookup"><span data-stu-id="c198b-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c198b-116">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="c198b-116">-EndTime</span></span>
<span data-ttu-id="c198b-117">Anger slut tiden för de schemalagda händelser som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c198b-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c198b-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c198b-118">-InformationAction</span></span>
<span data-ttu-id="c198b-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c198b-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c198b-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c198b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c198b-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="c198b-121">Continue</span></span>
- <span data-ttu-id="c198b-122">Över</span><span class="sxs-lookup"><span data-stu-id="c198b-122">Ignore</span></span>
- <span data-ttu-id="c198b-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="c198b-123">Inquire</span></span>
- <span data-ttu-id="c198b-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c198b-124">SilentlyContinue</span></span>
- <span data-ttu-id="c198b-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="c198b-125">Stop</span></span>
- <span data-ttu-id="c198b-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c198b-126">Suspend</span></span>

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

### <span data-ttu-id="c198b-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c198b-127">-InformationVariable</span></span>
<span data-ttu-id="c198b-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c198b-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c198b-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="c198b-129">-Profile</span></span>
<span data-ttu-id="c198b-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c198b-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c198b-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c198b-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c198b-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c198b-132">-ServiceName</span></span>
<span data-ttu-id="c198b-133">Anger namnet på den värdbaserade tjänst där denna cmdlet ska schemalägga händelser.</span><span class="sxs-lookup"><span data-stu-id="c198b-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

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

### <span data-ttu-id="c198b-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="c198b-134">-Slot</span></span>
<span data-ttu-id="c198b-135">Anger miljön för den distribution för vilken denna cmdlet ska schemalägga händelser.</span><span class="sxs-lookup"><span data-stu-id="c198b-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="c198b-136">Giltiga värden är: för produktion och produktion.</span><span class="sxs-lookup"><span data-stu-id="c198b-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="c198b-137">Standardvärdet är produktion.</span><span class="sxs-lookup"><span data-stu-id="c198b-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c198b-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c198b-138">-StartTime</span></span>
<span data-ttu-id="c198b-139">Anger start tiden för de schemalagda händelser som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c198b-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c198b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c198b-140">CommonParameters</span></span>
<span data-ttu-id="c198b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c198b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c198b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c198b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c198b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c198b-143">INPUTS</span></span>

## <span data-ttu-id="c198b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c198b-144">OUTPUTS</span></span>

## <span data-ttu-id="c198b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c198b-145">NOTES</span></span>

## <span data-ttu-id="c198b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c198b-146">RELATED LINKS</span></span>

[<span data-ttu-id="c198b-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c198b-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


