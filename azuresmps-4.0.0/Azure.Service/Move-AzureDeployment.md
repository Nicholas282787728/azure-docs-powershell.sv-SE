---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099474"
---
# <span data-ttu-id="ff89f-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff89f-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="ff89f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff89f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff89f-103">Byter plats på distributioner mellan produktion och mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="ff89f-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="ff89f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff89f-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff89f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff89f-105">DESCRIPTION</span></span>
<span data-ttu-id="ff89f-106">Cmdleten **Move-AzureDeployment** byter plats på de virtuella IP-adresserna för distributioner i produktions-och mellanliggande miljöer.</span><span class="sxs-lookup"><span data-stu-id="ff89f-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="ff89f-107">Denna cmdlet byter plats på en distribution som körs i mellanlagringsdatabasen till produktions miljön och en distribution som körs i produktions miljön till utvecklings miljön.</span><span class="sxs-lookup"><span data-stu-id="ff89f-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="ff89f-108">Om det finns en distribution i utvecklings miljön och ingen distribution i produktions miljön flyttar cmdleten distributionen till produktion.</span><span class="sxs-lookup"><span data-stu-id="ff89f-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="ff89f-109">Om det finns en distribution i produktions miljön och ingen distribution i mellanlagringsdatabasen Miss lyckas cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff89f-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="ff89f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff89f-110">EXAMPLES</span></span>

### <span data-ttu-id="ff89f-111">Exempel 1: byta distributioner för en tjänst</span><span class="sxs-lookup"><span data-stu-id="ff89f-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="ff89f-112">Det här kommandot byter plats på distributionerna av tjänsten som heter ContosoService mellan produktions-och mellanliggande miljöer.</span><span class="sxs-lookup"><span data-stu-id="ff89f-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="ff89f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff89f-113">PARAMETERS</span></span>

### <span data-ttu-id="ff89f-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff89f-114">-InformationAction</span></span>
<span data-ttu-id="ff89f-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ff89f-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff89f-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ff89f-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff89f-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="ff89f-117">Continue</span></span>
- <span data-ttu-id="ff89f-118">Över</span><span class="sxs-lookup"><span data-stu-id="ff89f-118">Ignore</span></span>
- <span data-ttu-id="ff89f-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="ff89f-119">Inquire</span></span>
- <span data-ttu-id="ff89f-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff89f-120">SilentlyContinue</span></span>
- <span data-ttu-id="ff89f-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="ff89f-121">Stop</span></span>
- <span data-ttu-id="ff89f-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ff89f-122">Suspend</span></span>

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

### <span data-ttu-id="ff89f-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff89f-123">-InformationVariable</span></span>
<span data-ttu-id="ff89f-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ff89f-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff89f-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff89f-125">-Profile</span></span>
<span data-ttu-id="ff89f-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ff89f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff89f-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ff89f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff89f-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ff89f-128">-ServiceName</span></span>
<span data-ttu-id="ff89f-129">Anger namnet på den tjänst där denna cmdlet byter plats för produktion och mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="ff89f-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="ff89f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff89f-130">CommonParameters</span></span>
<span data-ttu-id="ff89f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff89f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff89f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff89f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff89f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff89f-133">INPUTS</span></span>

## <span data-ttu-id="ff89f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff89f-134">OUTPUTS</span></span>

### <span data-ttu-id="ff89f-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="ff89f-135">ManagementOperationContext</span></span>

## <span data-ttu-id="ff89f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff89f-136">NOTES</span></span>

## <span data-ttu-id="ff89f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff89f-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff89f-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff89f-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="ff89f-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="ff89f-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="ff89f-140">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff89f-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="ff89f-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff89f-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="ff89f-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff89f-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


