---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571031"
---
# <span data-ttu-id="a402a-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a402a-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="a402a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a402a-102">SYNOPSIS</span></span>
<span data-ttu-id="a402a-103">Läser in Azure-autentiseringsinformation från en fil.</span><span class="sxs-lookup"><span data-stu-id="a402a-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="a402a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a402a-104">SYNTAX</span></span>

### <span data-ttu-id="a402a-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="a402a-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a402a-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="a402a-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a402a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a402a-107">DESCRIPTION</span></span>
<span data-ttu-id="a402a-108">Import-AzureRmContext cmdlet läser in autentiseringsinformation från en fil för att ange Azure-miljön och-kontexten.</span><span class="sxs-lookup"><span data-stu-id="a402a-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="a402a-109">Cmdlets som du kör i den aktuella sessionen använder den här informationen för att autentisera förfrågningar till Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a402a-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="a402a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a402a-110">EXAMPLES</span></span>

### <span data-ttu-id="a402a-111">Exempel 1: importera en kontext från en AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a402a-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a402a-112">I det här exemplet importeras en kontext från en PSAzureProfile som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a402a-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="a402a-113">Exempel 2: importera en kontext från en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="a402a-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a402a-114">Det här exemplet väljer en kontext från en JSON-fil som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a402a-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="a402a-115">Du kan skapa den här JSON-filen från import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="a402a-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="a402a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a402a-116">PARAMETERS</span></span>

### <span data-ttu-id="a402a-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="a402a-117">-AzureContext</span></span>
<span data-ttu-id="a402a-118">Anger den Azure-kontext från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a402a-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="a402a-119">Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.</span><span class="sxs-lookup"><span data-stu-id="a402a-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a402a-120">-Path</span><span class="sxs-lookup"><span data-stu-id="a402a-120">-Path</span></span>
<span data-ttu-id="a402a-121">Anger sökvägen till kontext information som sparats med AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="a402a-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a402a-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a402a-122">-Confirm</span></span>
<span data-ttu-id="a402a-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a402a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a402a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a402a-124">-WhatIf</span></span>
<span data-ttu-id="a402a-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a402a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a402a-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a402a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a402a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a402a-127">INPUTS</span></span>

### <span data-ttu-id="a402a-128">Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="a402a-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="a402a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a402a-129">System.String</span></span>

## <span data-ttu-id="a402a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a402a-130">OUTPUTS</span></span>

### <span data-ttu-id="a402a-131">Microsoft. Azure. commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a402a-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="a402a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a402a-132">NOTES</span></span>

## <span data-ttu-id="a402a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a402a-133">RELATED LINKS</span></span>

