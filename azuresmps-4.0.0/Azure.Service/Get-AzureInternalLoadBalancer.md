---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099570"
---
# <span data-ttu-id="65da9-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65da9-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="65da9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65da9-102">SYNOPSIS</span></span>
<span data-ttu-id="65da9-103">Hämtar information om intern belastnings Utjämnings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="65da9-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="65da9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65da9-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="65da9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65da9-105">DESCRIPTION</span></span>
<span data-ttu-id="65da9-106">Cmdleten **Get-AzureInternalLoadBalancer** hämtar information om den interna belastningsutjämnaren för en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="65da9-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="65da9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65da9-107">EXAMPLES</span></span>

### <span data-ttu-id="65da9-108">Exempel 1: få information för en intern belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="65da9-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="65da9-109">Det här kommandot får tjänsten som heter ContosoService med hjälp av cmdleten **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="65da9-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="65da9-110">Kommandot överför denna tjänst till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="65da9-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="65da9-111">Den aktuella cmdleten hämtar information för den interna belastningsutjämnaren för den tjänsten.</span><span class="sxs-lookup"><span data-stu-id="65da9-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="65da9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65da9-112">PARAMETERS</span></span>

### <span data-ttu-id="65da9-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="65da9-113">-InformationAction</span></span>
<span data-ttu-id="65da9-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="65da9-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="65da9-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="65da9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="65da9-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="65da9-116">Continue</span></span>
- <span data-ttu-id="65da9-117">Över</span><span class="sxs-lookup"><span data-stu-id="65da9-117">Ignore</span></span>
- <span data-ttu-id="65da9-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="65da9-118">Inquire</span></span>
- <span data-ttu-id="65da9-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="65da9-119">SilentlyContinue</span></span>
- <span data-ttu-id="65da9-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="65da9-120">Stop</span></span>
- <span data-ttu-id="65da9-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="65da9-121">Suspend</span></span>

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

### <span data-ttu-id="65da9-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="65da9-122">-InformationVariable</span></span>
<span data-ttu-id="65da9-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="65da9-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="65da9-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="65da9-124">-Profile</span></span>
<span data-ttu-id="65da9-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="65da9-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65da9-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="65da9-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65da9-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="65da9-127">-ServiceName</span></span>
<span data-ttu-id="65da9-128">Anger namnet på den tjänst där denna cmdlet hämtar information för en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="65da9-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

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

### <span data-ttu-id="65da9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65da9-129">CommonParameters</span></span>
<span data-ttu-id="65da9-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65da9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65da9-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65da9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65da9-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65da9-132">INPUTS</span></span>

## <span data-ttu-id="65da9-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65da9-133">OUTPUTS</span></span>

### <span data-ttu-id="65da9-134">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="65da9-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="65da9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65da9-135">NOTES</span></span>

## <span data-ttu-id="65da9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65da9-136">RELATED LINKS</span></span>

[<span data-ttu-id="65da9-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65da9-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="65da9-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="65da9-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="65da9-139">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="65da9-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="65da9-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65da9-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="65da9-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65da9-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


