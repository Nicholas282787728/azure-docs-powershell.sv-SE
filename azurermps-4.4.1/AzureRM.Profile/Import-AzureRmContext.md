---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577536"
---
# <span data-ttu-id="4039f-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4039f-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="4039f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4039f-102">SYNOPSIS</span></span>
<span data-ttu-id="4039f-103">Läser in Azure-autentiseringsinformation från en fil.</span><span class="sxs-lookup"><span data-stu-id="4039f-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4039f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4039f-104">SYNTAX</span></span>

### <span data-ttu-id="4039f-105">ProfileFromDisk (standard)</span><span class="sxs-lookup"><span data-stu-id="4039f-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4039f-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="4039f-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4039f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4039f-107">DESCRIPTION</span></span>
<span data-ttu-id="4039f-108">Import-AzureRmContext cmdlet läser in autentiseringsinformation från en fil för att ange Azure-miljön och-kontexten.</span><span class="sxs-lookup"><span data-stu-id="4039f-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="4039f-109">Cmdlets som du kör i den aktuella sessionen använder den här informationen för att autentisera förfrågningar till Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4039f-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="4039f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4039f-110">EXAMPLES</span></span>

### <span data-ttu-id="4039f-111">Exempel 1: importera en kontext från en AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="4039f-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="4039f-112">I det här exemplet importeras en kontext från en PSAzureProfile som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4039f-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="4039f-113">Exempel 2: importera en kontext från en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="4039f-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="4039f-114">Det här exemplet väljer en kontext från en JSON-fil som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4039f-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="4039f-115">Denna JSON-fil kan skapas från Save-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="4039f-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="4039f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4039f-116">PARAMETERS</span></span>

### <span data-ttu-id="4039f-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="4039f-117">-AzureContext</span></span>
<span data-ttu-id="4039f-118">Anger den Azure-kontext från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4039f-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="4039f-119">Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.</span><span class="sxs-lookup"><span data-stu-id="4039f-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4039f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4039f-120">-DefaultProfile</span></span>
<span data-ttu-id="4039f-121">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4039f-121">The credentials, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039f-122">-Path</span><span class="sxs-lookup"><span data-stu-id="4039f-122">-Path</span></span>
<span data-ttu-id="4039f-123">Anger sökvägen till kontext information som sparats med AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="4039f-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4039f-124">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="4039f-124">-Scope</span></span>
<span data-ttu-id="4039f-125">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="4039f-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4039f-126">-Confirm</span></span>
<span data-ttu-id="4039f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4039f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4039f-128">-WhatIf</span></span>
<span data-ttu-id="4039f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4039f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4039f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4039f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4039f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4039f-131">CommonParameters</span></span>
<span data-ttu-id="4039f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4039f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4039f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4039f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4039f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4039f-134">INPUTS</span></span>

### <span data-ttu-id="4039f-135">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="4039f-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="4039f-136">Innehåller den uppsättning autentiseringsuppgifter, konton och prenumerationer som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4039f-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="4039f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4039f-137">OUTPUTS</span></span>

### <span data-ttu-id="4039f-138">Microsoft. Azure. commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="4039f-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="4039f-139">Innehåller den uppsättning autentiseringsuppgifter, konton och prenumerationer som kan användas för att kommunicera med Azure.</span><span class="sxs-lookup"><span data-stu-id="4039f-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="4039f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4039f-140">NOTES</span></span>

## <span data-ttu-id="4039f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4039f-141">RELATED LINKS</span></span>

