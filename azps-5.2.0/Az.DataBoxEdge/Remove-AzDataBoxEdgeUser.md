---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406067"
---
# <span data-ttu-id="a5b56-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a5b56-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="a5b56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5b56-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b56-103">Tar bort en användare på en enhet.</span><span class="sxs-lookup"><span data-stu-id="a5b56-103">Removes a user on a device.</span></span>

## <span data-ttu-id="a5b56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5b56-104">SYNTAX</span></span>

### <span data-ttu-id="a5b56-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a5b56-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b56-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b56-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b56-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b56-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b56-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5b56-108">DESCRIPTION</span></span>
<span data-ttu-id="a5b56-109">Cmdleten **Remove-AzDataBoxEdgeUser** tar bort en användare i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="a5b56-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="a5b56-110">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="a5b56-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="a5b56-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5b56-111">EXAMPLES</span></span>

### <span data-ttu-id="a5b56-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5b56-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="a5b56-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5b56-113">PARAMETERS</span></span>

### <span data-ttu-id="a5b56-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5b56-114">-AsJob</span></span>
<span data-ttu-id="a5b56-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a5b56-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5b56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b56-116">-DefaultProfile</span></span>
<span data-ttu-id="a5b56-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b56-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="a5b56-118">-DeviceName</span></span>
<span data-ttu-id="a5b56-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="a5b56-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b56-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b56-120">-InputObject</span></span>
<span data-ttu-id="a5b56-121">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="a5b56-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5b56-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5b56-122">-Name</span></span>
<span data-ttu-id="a5b56-123">Namnen</span><span class="sxs-lookup"><span data-stu-id="a5b56-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b56-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5b56-124">-PassThru</span></span>
<span data-ttu-id="a5b56-125">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="a5b56-125">returns true if successful</span></span>

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

### <span data-ttu-id="a5b56-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b56-126">-ResourceGroupName</span></span>
<span data-ttu-id="a5b56-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a5b56-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b56-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b56-128">-ResourceId</span></span>
<span data-ttu-id="a5b56-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b56-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="a5b56-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5b56-130">-Confirm</span></span>
<span data-ttu-id="a5b56-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5b56-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b56-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b56-132">-WhatIf</span></span>
<span data-ttu-id="a5b56-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5b56-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5b56-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5b56-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b56-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b56-135">CommonParameters</span></span>
<span data-ttu-id="a5b56-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b56-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b56-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5b56-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b56-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5b56-138">INPUTS</span></span>

### <span data-ttu-id="a5b56-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b56-139">System.String</span></span>

### <span data-ttu-id="a5b56-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a5b56-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="a5b56-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5b56-141">OUTPUTS</span></span>

### <span data-ttu-id="a5b56-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a5b56-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a5b56-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5b56-143">NOTES</span></span>

## <span data-ttu-id="a5b56-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5b56-144">RELATED LINKS</span></span>
