---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271863"
---
# <span data-ttu-id="9c3ef-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="9c3ef-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="9c3ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3ef-103">Registrerar ett verktyg med det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="9c3ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c3ef-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c3ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="9c3ef-106">Registrerar ett verktyg med det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="9c3ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="9c3ef-108">Exempel 1: verktyget registrera.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="9c3ef-109">Registrerar ett verktyg med det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="9c3ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c3ef-110">PARAMETERS</span></span>

### <span data-ttu-id="9c3ef-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="9c3ef-111">-AcceptLanguage</span></span>
<span data-ttu-id="9c3ef-112">Standard rubrik för begäran.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-112">Standard request header.</span></span>
<span data-ttu-id="9c3ef-113">Används av tjänst för att svara på klienten på lämpligt språk.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="9c3ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3ef-114">-DefaultProfile</span></span>
<span data-ttu-id="9c3ef-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c3ef-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="9c3ef-116">-MigrateProjectName</span></span>
<span data-ttu-id="9c3ef-117">Namn på Azure Migrate Project.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="9c3ef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3ef-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c3ef-119">Namnet på den Azure Resource-grupp som migrerar Project.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="9c3ef-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c3ef-120">-SubscriptionId</span></span>
<span data-ttu-id="9c3ef-121">ID för Azure-prenumeration som migrerar projektet skapades med.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="9c3ef-122">-Verktyg</span><span class="sxs-lookup"><span data-stu-id="9c3ef-122">-Tool</span></span>
<span data-ttu-id="9c3ef-123">Hämtar eller anger det verktyg som ska registreras.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="9c3ef-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c3ef-124">-Confirm</span></span>
<span data-ttu-id="9c3ef-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c3ef-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c3ef-126">-WhatIf</span></span>
<span data-ttu-id="9c3ef-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c3ef-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c3ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3ef-129">CommonParameters</span></span>
<span data-ttu-id="9c3ef-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3ef-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c3ef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3ef-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c3ef-132">INPUTS</span></span>

## <span data-ttu-id="9c3ef-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c3ef-133">OUTPUTS</span></span>

### <span data-ttu-id="9c3ef-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c3ef-134">System.Boolean</span></span>

## <span data-ttu-id="9c3ef-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c3ef-135">NOTES</span></span>

<span data-ttu-id="9c3ef-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c3ef-136">ALIASES</span></span>

## <span data-ttu-id="9c3ef-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c3ef-137">RELATED LINKS</span></span>

