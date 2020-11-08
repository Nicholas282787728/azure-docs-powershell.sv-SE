---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269521"
---
# <span data-ttu-id="cd0e5-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="cd0e5-101">Import-AzContext</span></span>

## <span data-ttu-id="cd0e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0e5-103">Läser in Azure-autentiseringsinformation från en fil.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="cd0e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd0e5-104">SYNTAX</span></span>

### <span data-ttu-id="cd0e5-105">ProfileFromDisk (standard)</span><span class="sxs-lookup"><span data-stu-id="cd0e5-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd0e5-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e5-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0e5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd0e5-107">DESCRIPTION</span></span>
<span data-ttu-id="cd0e5-108">Import-AzContext cmdlet läser in autentiseringsinformation från en fil för att ange Azure-miljön och-kontexten.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="cd0e5-109">Cmdlets som du kör i den aktuella sessionen använder den här informationen för att autentisera förfrågningar till Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="cd0e5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd0e5-110">EXAMPLES</span></span>

### <span data-ttu-id="cd0e5-111">Exempel 1: importera en kontext från en AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e5-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="cd0e5-112">I det här exemplet importeras en kontext från en PSAzureProfile som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="cd0e5-113">Exempel 2: importera en kontext från en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="cd0e5-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="cd0e5-114">Det här exemplet väljer en kontext från en JSON-fil som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="cd0e5-115">Denna JSON-fil kan skapas från Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="cd0e5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd0e5-116">PARAMETERS</span></span>

### <span data-ttu-id="cd0e5-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="cd0e5-117">-AzureContext</span></span>
<span data-ttu-id="cd0e5-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="cd0e5-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="cd0e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e5-119">-DefaultProfile</span></span>
<span data-ttu-id="cd0e5-120">Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cd0e5-120">The credentials, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-121">-Path</span><span class="sxs-lookup"><span data-stu-id="cd0e5-121">-Path</span></span>
<span data-ttu-id="cd0e5-122">Anger sökvägen till kontext information som sparats med AzContext.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="cd0e5-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="cd0e5-123">-Scope</span></span>
<span data-ttu-id="cd0e5-124">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="cd0e5-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd0e5-125">-Confirm</span></span>
<span data-ttu-id="cd0e5-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd0e5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0e5-127">-WhatIf</span></span>
<span data-ttu-id="cd0e5-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd0e5-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd0e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0e5-130">CommonParameters</span></span>
<span data-ttu-id="cd0e5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0e5-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0e5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0e5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd0e5-133">INPUTS</span></span>

### <span data-ttu-id="cd0e5-134">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e5-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="cd0e5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cd0e5-135">System.String</span></span>

## <span data-ttu-id="cd0e5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd0e5-136">OUTPUTS</span></span>

### <span data-ttu-id="cd0e5-137">Microsoft. Azure. commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="cd0e5-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="cd0e5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd0e5-138">NOTES</span></span>

## <span data-ttu-id="cd0e5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd0e5-139">RELATED LINKS</span></span>
