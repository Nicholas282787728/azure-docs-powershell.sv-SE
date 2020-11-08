---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269672"
---
# <span data-ttu-id="dfd99-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="dfd99-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="dfd99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfd99-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd99-103">Kontrollerar om namnet på konfigurations lagret är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="dfd99-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="dfd99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfd99-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfd99-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfd99-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd99-106">Kontrollerar om namnet på konfigurations lagret är tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="dfd99-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="dfd99-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfd99-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd99-108">Exempel 1: testa tillgänglighet för app Configuration Store-namnet</span><span class="sxs-lookup"><span data-stu-id="dfd99-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="dfd99-109">Det här kommandot testar tillgänglighet för app Configuration Store-namnet.</span><span class="sxs-lookup"><span data-stu-id="dfd99-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="dfd99-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfd99-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd99-111">-DefaultProfile</span></span>
<span data-ttu-id="dfd99-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfd99-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfd99-113">-Name</span></span>
<span data-ttu-id="dfd99-114">Namnet för att kontrol lera tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="dfd99-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="dfd99-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfd99-115">-SubscriptionId</span></span>
<span data-ttu-id="dfd99-116">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="dfd99-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd99-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfd99-117">-Confirm</span></span>
<span data-ttu-id="dfd99-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfd99-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd99-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd99-119">-WhatIf</span></span>
<span data-ttu-id="dfd99-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfd99-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd99-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfd99-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd99-122">CommonParameters</span></span>
<span data-ttu-id="dfd99-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd99-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfd99-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd99-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfd99-125">INPUTS</span></span>

## <span data-ttu-id="dfd99-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfd99-126">OUTPUTS</span></span>

### <span data-ttu-id="dfd99-127">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="dfd99-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="dfd99-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfd99-128">NOTES</span></span>

<span data-ttu-id="dfd99-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dfd99-129">ALIASES</span></span>

## <span data-ttu-id="dfd99-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfd99-130">RELATED LINKS</span></span>

