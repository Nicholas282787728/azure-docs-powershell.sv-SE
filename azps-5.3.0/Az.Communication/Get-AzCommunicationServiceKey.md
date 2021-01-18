---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524575"
---
# <span data-ttu-id="faff5-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="faff5-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="faff5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="faff5-102">SYNOPSIS</span></span>
<span data-ttu-id="faff5-103">Hämta åtkomst nycklar för CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="faff5-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="faff5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="faff5-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faff5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="faff5-105">DESCRIPTION</span></span>
<span data-ttu-id="faff5-106">Hämta åtkomst nycklar för CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="faff5-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="faff5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="faff5-107">EXAMPLES</span></span>

### <span data-ttu-id="faff5-108">Exempel 1: Hämta tangenten för den angivna kommunikation-tjänsten</span><span class="sxs-lookup"><span data-stu-id="faff5-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="faff5-109">Visar ConnectionString och tangenten för den angivna kommunikation-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="faff5-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="faff5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="faff5-110">PARAMETERS</span></span>

### <span data-ttu-id="faff5-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="faff5-111">-CommunicationServiceName</span></span>
<span data-ttu-id="faff5-112">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="faff5-112">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faff5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faff5-113">-DefaultProfile</span></span>
<span data-ttu-id="faff5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="faff5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faff5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faff5-115">-ResourceGroupName</span></span>
<span data-ttu-id="faff5-116">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="faff5-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="faff5-117">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="faff5-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faff5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faff5-118">-SubscriptionId</span></span>
<span data-ttu-id="faff5-119">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="faff5-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="faff5-120">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="faff5-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faff5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="faff5-121">-Confirm</span></span>
<span data-ttu-id="faff5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="faff5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faff5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faff5-123">-WhatIf</span></span>
<span data-ttu-id="faff5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="faff5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faff5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="faff5-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faff5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faff5-126">CommonParameters</span></span>
<span data-ttu-id="faff5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faff5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faff5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faff5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faff5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="faff5-129">INPUTS</span></span>

## <span data-ttu-id="faff5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="faff5-130">OUTPUTS</span></span>

### <span data-ttu-id="faff5-131">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="faff5-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="faff5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="faff5-132">NOTES</span></span>

<span data-ttu-id="faff5-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="faff5-133">ALIASES</span></span>

## <span data-ttu-id="faff5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="faff5-134">RELATED LINKS</span></span>

