---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/import-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: 590557d883979ac3f23decd88695695df9aecc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576828"
---
# <span data-ttu-id="448fa-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="448fa-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="448fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="448fa-102">SYNOPSIS</span></span>
<span data-ttu-id="448fa-103">Läser in Azure-autentiseringsinformation från en fil.</span><span class="sxs-lookup"><span data-stu-id="448fa-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="448fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="448fa-104">SYNTAX</span></span>

### <span data-ttu-id="448fa-105">ProfileFromDisk (standard)</span><span class="sxs-lookup"><span data-stu-id="448fa-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448fa-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="448fa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="448fa-107">DESCRIPTION</span></span>
<span data-ttu-id="448fa-108">Import-AzureRmContext cmdlet läser in autentiseringsinformation från en fil för att ange Azure-miljön och-kontexten.</span><span class="sxs-lookup"><span data-stu-id="448fa-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="448fa-109">Cmdlets som du kör i den aktuella sessionen använder den här informationen för att autentisera förfrågningar till Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="448fa-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="448fa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="448fa-110">EXAMPLES</span></span>

### <span data-ttu-id="448fa-111">Exempel 1: importera en kontext från en AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Connect-AzureRmAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="448fa-112">I det här exemplet importeras en kontext från en PSAzureProfile som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="448fa-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="448fa-113">Exempel 2: importera en kontext från en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="448fa-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="448fa-114">Det här exemplet väljer en kontext från en JSON-fil som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="448fa-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="448fa-115">Denna JSON-fil kan skapas från Save-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="448fa-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="448fa-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="448fa-116">PARAMETERS</span></span>

### <span data-ttu-id="448fa-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="448fa-117">-AzureContext</span></span>
<span data-ttu-id="448fa-118">Anger den Azure-kontext från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="448fa-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="448fa-119">Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.</span><span class="sxs-lookup"><span data-stu-id="448fa-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="448fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-120">-DefaultProfile</span></span>
<span data-ttu-id="448fa-121">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="448fa-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="448fa-122">-Path</span><span class="sxs-lookup"><span data-stu-id="448fa-122">-Path</span></span>
<span data-ttu-id="448fa-123">Anger sökvägen till kontext information som sparats med AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="448fa-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

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

### <span data-ttu-id="448fa-124">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="448fa-124">-Scope</span></span>
<span data-ttu-id="448fa-125">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="448fa-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="448fa-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="448fa-126">-Confirm</span></span>
<span data-ttu-id="448fa-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="448fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448fa-128">-WhatIf</span></span>
<span data-ttu-id="448fa-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="448fa-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="448fa-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="448fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448fa-131">CommonParameters</span></span>
<span data-ttu-id="448fa-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448fa-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448fa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448fa-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="448fa-134">INPUTS</span></span>

### <span data-ttu-id="448fa-135">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="448fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="448fa-136">System.String</span></span>

## <span data-ttu-id="448fa-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="448fa-137">OUTPUTS</span></span>

### <span data-ttu-id="448fa-138">Microsoft. Azure. commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="448fa-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="448fa-139">NOTES</span></span>

## <span data-ttu-id="448fa-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="448fa-140">RELATED LINKS</span></span>
