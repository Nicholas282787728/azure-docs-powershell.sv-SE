---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524644"
---
# <span data-ttu-id="11bb5-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="11bb5-101">New-AzBotService</span></span>

## <span data-ttu-id="11bb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="11bb5-103">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="11bb5-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="11bb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11bb5-104">SYNTAX</span></span>

### <span data-ttu-id="11bb5-105">Registrering (standard)</span><span class="sxs-lookup"><span data-stu-id="11bb5-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11bb5-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="11bb5-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="11bb5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11bb5-107">DESCRIPTION</span></span>
<span data-ttu-id="11bb5-108">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="11bb5-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="11bb5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11bb5-109">EXAMPLES</span></span>

### <span data-ttu-id="11bb5-110">Exempel 1: skapa en ny robot</span><span class="sxs-lookup"><span data-stu-id="11bb5-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="11bb5-111">Skapa en ny robot enligt ResourceGroupName och ApplicationId</span><span class="sxs-lookup"><span data-stu-id="11bb5-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="11bb5-112">Exempel 2: skapa en ny webbapp</span><span class="sxs-lookup"><span data-stu-id="11bb5-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="11bb5-113">Skapa en ny webbapp genom ResourceGroupName och ApplicationId</span><span class="sxs-lookup"><span data-stu-id="11bb5-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="11bb5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11bb5-114">PARAMETERS</span></span>

### <span data-ttu-id="11bb5-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="11bb5-115">-ApplicationId</span></span>


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

### <span data-ttu-id="11bb5-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="11bb5-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="11bb5-117">-BotTemplateType</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bb5-118">-DefaultProfile</span></span>
<span data-ttu-id="11bb5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11bb5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11bb5-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="11bb5-120">-Description</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11bb5-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-122">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="11bb5-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="11bb5-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-124">-Språk</span><span class="sxs-lookup"><span data-stu-id="11bb5-124">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="11bb5-125">-Location</span></span>


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

### <span data-ttu-id="11bb5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="11bb5-126">-Name</span></span>
<span data-ttu-id="11bb5-127">Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="11bb5-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-128">-Registrering</span><span class="sxs-lookup"><span data-stu-id="11bb5-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bb5-129">-ResourceGroupName</span></span>
<span data-ttu-id="11bb5-130">Namnet på robot resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="11bb5-130">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="11bb5-131">-Sku</span></span>
<span data-ttu-id="11bb5-132">SKU-namnet</span><span class="sxs-lookup"><span data-stu-id="11bb5-132">The sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11bb5-133">-SubscriptionId</span></span>
<span data-ttu-id="11bb5-134">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="11bb5-134">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="11bb5-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="11bb5-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bb5-136">CommonParameters</span></span>
<span data-ttu-id="11bb5-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bb5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bb5-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11bb5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bb5-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11bb5-139">INPUTS</span></span>

## <span data-ttu-id="11bb5-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11bb5-140">OUTPUTS</span></span>

### <span data-ttu-id="11bb5-141">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="11bb5-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="11bb5-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11bb5-142">NOTES</span></span>

<span data-ttu-id="11bb5-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="11bb5-143">ALIASES</span></span>

## <span data-ttu-id="11bb5-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11bb5-144">RELATED LINKS</span></span>

