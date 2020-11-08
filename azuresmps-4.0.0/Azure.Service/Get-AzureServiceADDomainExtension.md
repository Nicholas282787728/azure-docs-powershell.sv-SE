---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093333"
---
# <span data-ttu-id="19db9-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="19db9-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="19db9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19db9-102">SYNOPSIS</span></span>
<span data-ttu-id="19db9-103">Hämtar det AD-domännamn (Cloud Service Active Directory) som gäller för alla roller eller till namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="19db9-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="19db9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19db9-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19db9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19db9-105">DESCRIPTION</span></span>
<span data-ttu-id="19db9-106">Cmdleten **Get-AzureServiceADDomainExtension** får till gång till moln tjänstens AD-tillägg som gäller för alla roller eller namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="19db9-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="19db9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19db9-107">EXAMPLES</span></span>

### <span data-ttu-id="19db9-108">Exempel 1: Hämta AD-domänen för en viss tjänst</span><span class="sxs-lookup"><span data-stu-id="19db9-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="19db9-109">Det här kommandot får AD-domännamnet för tjänsten som anges i $Svc.</span><span class="sxs-lookup"><span data-stu-id="19db9-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="19db9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19db9-110">PARAMETERS</span></span>

### <span data-ttu-id="19db9-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="19db9-111">-InformationAction</span></span>
<span data-ttu-id="19db9-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="19db9-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19db9-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="19db9-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19db9-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="19db9-114">Continue</span></span>
- <span data-ttu-id="19db9-115">Över</span><span class="sxs-lookup"><span data-stu-id="19db9-115">Ignore</span></span>
- <span data-ttu-id="19db9-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="19db9-116">Inquire</span></span>
- <span data-ttu-id="19db9-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="19db9-117">SilentlyContinue</span></span>
- <span data-ttu-id="19db9-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="19db9-118">Stop</span></span>
- <span data-ttu-id="19db9-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="19db9-119">Suspend</span></span>

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

### <span data-ttu-id="19db9-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="19db9-120">-InformationVariable</span></span>
<span data-ttu-id="19db9-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="19db9-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19db9-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="19db9-122">-Profile</span></span>
<span data-ttu-id="19db9-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="19db9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19db9-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="19db9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19db9-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="19db9-125">-ServiceName</span></span>
<span data-ttu-id="19db9-126">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="19db9-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19db9-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="19db9-127">-Slot</span></span>
<span data-ttu-id="19db9-128">Anger distributions miljön.</span><span class="sxs-lookup"><span data-stu-id="19db9-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="19db9-129">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="19db9-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19db9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19db9-130">CommonParameters</span></span>
<span data-ttu-id="19db9-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19db9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19db9-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19db9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19db9-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19db9-133">INPUTS</span></span>

## <span data-ttu-id="19db9-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19db9-134">OUTPUTS</span></span>

## <span data-ttu-id="19db9-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19db9-135">NOTES</span></span>

## <span data-ttu-id="19db9-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19db9-136">RELATED LINKS</span></span>

[<span data-ttu-id="19db9-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="19db9-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="19db9-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="19db9-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


