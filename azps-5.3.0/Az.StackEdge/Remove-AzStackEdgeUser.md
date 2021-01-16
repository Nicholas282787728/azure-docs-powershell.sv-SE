---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418952"
---
# <span data-ttu-id="74337-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="74337-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="74337-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74337-102">SYNOPSIS</span></span>
<span data-ttu-id="74337-103">Tar bort en användare på en enhet.</span><span class="sxs-lookup"><span data-stu-id="74337-103">Removes a user on a device.</span></span>

## <span data-ttu-id="74337-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74337-104">SYNTAX</span></span>

### <span data-ttu-id="74337-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="74337-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74337-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74337-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74337-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74337-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74337-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74337-108">DESCRIPTION</span></span>
<span data-ttu-id="74337-109">Cmdleten **Remove-AzStackEdgeUser** tar bort en användare på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="74337-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="74337-110">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="74337-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="74337-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74337-111">EXAMPLES</span></span>

### <span data-ttu-id="74337-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="74337-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="74337-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74337-113">PARAMETERS</span></span>

### <span data-ttu-id="74337-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74337-114">-AsJob</span></span>
<span data-ttu-id="74337-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="74337-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74337-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74337-116">-DefaultProfile</span></span>
<span data-ttu-id="74337-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74337-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74337-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="74337-118">-DeviceName</span></span>
<span data-ttu-id="74337-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="74337-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74337-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74337-120">-InputObject</span></span>
<span data-ttu-id="74337-121">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="74337-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74337-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="74337-122">-Name</span></span>
<span data-ttu-id="74337-123">Namnen</span><span class="sxs-lookup"><span data-stu-id="74337-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74337-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74337-124">-PassThru</span></span>
<span data-ttu-id="74337-125">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="74337-125">returns true if successful</span></span>

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

### <span data-ttu-id="74337-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74337-126">-ResourceGroupName</span></span>
<span data-ttu-id="74337-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="74337-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74337-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74337-128">-ResourceId</span></span>
<span data-ttu-id="74337-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="74337-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74337-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74337-130">-Confirm</span></span>
<span data-ttu-id="74337-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74337-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74337-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74337-132">-WhatIf</span></span>
<span data-ttu-id="74337-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74337-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74337-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74337-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74337-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74337-135">CommonParameters</span></span>
<span data-ttu-id="74337-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74337-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74337-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74337-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74337-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74337-138">INPUTS</span></span>

### <span data-ttu-id="74337-139">System. String</span><span class="sxs-lookup"><span data-stu-id="74337-139">System.String</span></span>

### <span data-ttu-id="74337-140">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="74337-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="74337-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74337-141">OUTPUTS</span></span>

### <span data-ttu-id="74337-142">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="74337-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="74337-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74337-143">NOTES</span></span>

## <span data-ttu-id="74337-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74337-144">RELATED LINKS</span></span>
