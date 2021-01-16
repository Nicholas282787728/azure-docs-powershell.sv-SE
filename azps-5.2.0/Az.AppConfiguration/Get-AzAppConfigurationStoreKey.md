---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387837"
---
# <span data-ttu-id="3bfe6-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="3bfe6-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="3bfe6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="3bfe6-103">Visar snabb tangenten för det angivna konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="3bfe6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bfe6-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bfe6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bfe6-105">DESCRIPTION</span></span>
<span data-ttu-id="3bfe6-106">Visar snabb tangenten för det angivna konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="3bfe6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bfe6-107">EXAMPLES</span></span>

### <span data-ttu-id="3bfe6-108">Exempel 1: lista alla lagrings nycklar för en app Configuration Store</span><span class="sxs-lookup"><span data-stu-id="3bfe6-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="3bfe6-109">Det här kommandot visar alla lagrings nycklar för en app Configuration Store.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="3bfe6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bfe6-110">PARAMETERS</span></span>

### <span data-ttu-id="3bfe6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bfe6-111">-DefaultProfile</span></span>
<span data-ttu-id="3bfe6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bfe6-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bfe6-113">-Name</span></span>
<span data-ttu-id="3bfe6-114">Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="3bfe6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bfe6-115">-ResourceGroupName</span></span>
<span data-ttu-id="3bfe6-116">Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="3bfe6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bfe6-117">-SubscriptionId</span></span>
<span data-ttu-id="3bfe6-118">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-118">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="3bfe6-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3bfe6-119">-Confirm</span></span>
<span data-ttu-id="3bfe6-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bfe6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bfe6-121">-WhatIf</span></span>
<span data-ttu-id="3bfe6-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bfe6-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bfe6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bfe6-124">CommonParameters</span></span>
<span data-ttu-id="3bfe6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bfe6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bfe6-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bfe6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bfe6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bfe6-127">INPUTS</span></span>

## <span data-ttu-id="3bfe6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bfe6-128">OUTPUTS</span></span>

### <span data-ttu-id="3bfe6-129">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="3bfe6-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="3bfe6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bfe6-130">NOTES</span></span>

<span data-ttu-id="3bfe6-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3bfe6-131">ALIASES</span></span>

## <span data-ttu-id="3bfe6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bfe6-132">RELATED LINKS</span></span>

