---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270562"
---
# <span data-ttu-id="ecbf1-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="ecbf1-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="ecbf1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbf1-103">Tar bort registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="ecbf1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecbf1-104">SYNTAX</span></span>

### <span data-ttu-id="ecbf1-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="ecbf1-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbf1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecbf1-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecbf1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecbf1-107">DESCRIPTION</span></span>
<span data-ttu-id="ecbf1-108">Tar bort registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="ecbf1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecbf1-109">EXAMPLES</span></span>

### <span data-ttu-id="ecbf1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecbf1-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="ecbf1-111">Tar bort registrerings definitionen per namn i standard omfattningen.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="ecbf1-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ecbf1-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="ecbf1-113">Tar bort registrerings definitionen för detta objekt.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="ecbf1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecbf1-114">PARAMETERS</span></span>

### <span data-ttu-id="ecbf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbf1-115">-DefaultProfile</span></span>
<span data-ttu-id="ecbf1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecbf1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecbf1-117">-InputObject</span></span>
<span data-ttu-id="ecbf1-118">Registrerings definitions objekt.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecbf1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecbf1-119">-Name</span></span>
<span data-ttu-id="ecbf1-120">Det unika namnet på registrerings definitionen.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbf1-121">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="ecbf1-121">-Scope</span></span>
<span data-ttu-id="ecbf1-122">Omfattningen där registrerings definitionen skapades.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecbf1-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecbf1-123">-Confirm</span></span>
<span data-ttu-id="ecbf1-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecbf1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecbf1-125">-WhatIf</span></span>
<span data-ttu-id="ecbf1-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecbf1-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecbf1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbf1-128">CommonParameters</span></span>
<span data-ttu-id="ecbf1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbf1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbf1-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecbf1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbf1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecbf1-131">INPUTS</span></span>

### <span data-ttu-id="ecbf1-132">Microsoft. Azure. PowerShell. cmdletar. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="ecbf1-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="ecbf1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecbf1-133">OUTPUTS</span></span>

### <span data-ttu-id="ecbf1-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="ecbf1-134">System.Void</span></span>
## <span data-ttu-id="ecbf1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecbf1-135">NOTES</span></span>

## <span data-ttu-id="ecbf1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecbf1-136">RELATED LINKS</span></span>
