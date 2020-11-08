---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099016"
---
# <span data-ttu-id="06863-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="06863-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="06863-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06863-102">SYNOPSIS</span></span>
<span data-ttu-id="06863-103">Guidar den angivna uppgraderings domänen.</span><span class="sxs-lookup"><span data-stu-id="06863-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="06863-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06863-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="06863-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06863-105">DESCRIPTION</span></span>
<span data-ttu-id="06863-106">Cmdleten **set-AzureWalkUpgradeDomain** initierar den faktiska uppgraderingen av en Azure-distribution.</span><span class="sxs-lookup"><span data-stu-id="06863-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="06863-107">Uppgraderings paketet och konfigurationen är inställda genom att använda cmdleten **set-AzureDeployment** med-Upgrade-växeln.</span><span class="sxs-lookup"><span data-stu-id="06863-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="06863-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06863-108">EXAMPLES</span></span>

### <span data-ttu-id="06863-109">Exempel 1: initiera en uppgradering av en produktions distribution</span><span class="sxs-lookup"><span data-stu-id="06863-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="06863-110">Det här kommandot initierar uppgraderingen av uppgraderings domän 2 för produktions distributionen av MySvc1-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06863-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="06863-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06863-111">PARAMETERS</span></span>

### <span data-ttu-id="06863-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="06863-112">-DomainNumber</span></span>
<span data-ttu-id="06863-113">Anger den uppgraderings domän som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="06863-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06863-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="06863-114">-InformationAction</span></span>
<span data-ttu-id="06863-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="06863-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06863-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="06863-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06863-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="06863-117">Continue</span></span>
- <span data-ttu-id="06863-118">Över</span><span class="sxs-lookup"><span data-stu-id="06863-118">Ignore</span></span>
- <span data-ttu-id="06863-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="06863-119">Inquire</span></span>
- <span data-ttu-id="06863-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06863-120">SilentlyContinue</span></span>
- <span data-ttu-id="06863-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="06863-121">Stop</span></span>
- <span data-ttu-id="06863-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="06863-122">Suspend</span></span>

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

### <span data-ttu-id="06863-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06863-123">-InformationVariable</span></span>
<span data-ttu-id="06863-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="06863-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06863-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="06863-125">-Profile</span></span>
<span data-ttu-id="06863-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="06863-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06863-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="06863-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06863-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="06863-128">-ServiceName</span></span>
<span data-ttu-id="06863-129">Anger namnet på Microsoft Azure-tjänsten som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="06863-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

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

### <span data-ttu-id="06863-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="06863-130">-Slot</span></span>
<span data-ttu-id="06863-131">Anger miljön för distributionen som ska uppgraderas.</span><span class="sxs-lookup"><span data-stu-id="06863-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="06863-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="06863-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06863-133">Lagring</span><span class="sxs-lookup"><span data-stu-id="06863-133">Staging</span></span>
- <span data-ttu-id="06863-134">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="06863-134">Production</span></span>

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

### <span data-ttu-id="06863-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06863-135">CommonParameters</span></span>
<span data-ttu-id="06863-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06863-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06863-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06863-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06863-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06863-138">INPUTS</span></span>

## <span data-ttu-id="06863-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06863-139">OUTPUTS</span></span>

### <span data-ttu-id="06863-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="06863-140">ManagementOperationContext</span></span>

## <span data-ttu-id="06863-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06863-141">NOTES</span></span>

## <span data-ttu-id="06863-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06863-142">RELATED LINKS</span></span>

[<span data-ttu-id="06863-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="06863-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


