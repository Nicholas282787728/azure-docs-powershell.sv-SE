---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271858"
---
# <span data-ttu-id="cd293-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="cd293-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="cd293-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd293-102">SYNOPSIS</span></span>
<span data-ttu-id="cd293-103">Ta bort det migrerade projektet.</span><span class="sxs-lookup"><span data-stu-id="cd293-103">Delete the migrate project.</span></span>
<span data-ttu-id="cd293-104">Det går inte att ta bort projekt som inte finns.</span><span class="sxs-lookup"><span data-stu-id="cd293-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="cd293-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd293-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd293-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd293-106">DESCRIPTION</span></span>
<span data-ttu-id="cd293-107">Ta bort det migrerade projektet.</span><span class="sxs-lookup"><span data-stu-id="cd293-107">Delete the migrate project.</span></span>
<span data-ttu-id="cd293-108">Det går inte att ta bort projekt som inte finns.</span><span class="sxs-lookup"><span data-stu-id="cd293-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="cd293-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd293-109">EXAMPLES</span></span>

### <span data-ttu-id="cd293-110">Exempel 1: delete (standard)</span><span class="sxs-lookup"><span data-stu-id="cd293-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="cd293-111">Ta bort det migrerade projektet.</span><span class="sxs-lookup"><span data-stu-id="cd293-111">Delete the migrate project.</span></span>
<span data-ttu-id="cd293-112">Det går inte att ta bort projekt som inte finns.</span><span class="sxs-lookup"><span data-stu-id="cd293-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="cd293-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd293-113">PARAMETERS</span></span>

### <span data-ttu-id="cd293-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="cd293-114">-AcceptLanguage</span></span>
<span data-ttu-id="cd293-115">Standard rubrik för begäran.</span><span class="sxs-lookup"><span data-stu-id="cd293-115">Standard request header.</span></span>
<span data-ttu-id="cd293-116">Används av tjänst för att svara på klienten på lämpligt språk.</span><span class="sxs-lookup"><span data-stu-id="cd293-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="cd293-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd293-117">-DefaultProfile</span></span>
<span data-ttu-id="cd293-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd293-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd293-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd293-119">-Name</span></span>
<span data-ttu-id="cd293-120">Namn på Azure Migrate Project.</span><span class="sxs-lookup"><span data-stu-id="cd293-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd293-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd293-121">-PassThru</span></span>
<span data-ttu-id="cd293-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="cd293-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd293-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd293-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd293-124">Namnet på den Azure Resource-grupp som migrerar Project.</span><span class="sxs-lookup"><span data-stu-id="cd293-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="cd293-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd293-125">-SubscriptionId</span></span>
<span data-ttu-id="cd293-126">ID för Azure-prenumeration som migrerar projektet skapades med.</span><span class="sxs-lookup"><span data-stu-id="cd293-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="cd293-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd293-127">-Confirm</span></span>
<span data-ttu-id="cd293-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd293-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd293-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd293-129">-WhatIf</span></span>
<span data-ttu-id="cd293-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd293-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd293-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd293-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd293-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd293-132">CommonParameters</span></span>
<span data-ttu-id="cd293-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd293-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd293-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd293-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd293-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd293-135">INPUTS</span></span>

## <span data-ttu-id="cd293-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd293-136">OUTPUTS</span></span>

### <span data-ttu-id="cd293-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd293-137">System.Boolean</span></span>

## <span data-ttu-id="cd293-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd293-138">NOTES</span></span>

<span data-ttu-id="cd293-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd293-139">ALIASES</span></span>

## <span data-ttu-id="cd293-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd293-140">RELATED LINKS</span></span>

