---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 1d6c99a44e2163f2d441dcacc87cf202f334f330
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922993"
---
# <span data-ttu-id="b5980-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b5980-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b5980-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5980-102">SYNOPSIS</span></span>
<span data-ttu-id="b5980-103">Tar bort en användare på en enhet.</span><span class="sxs-lookup"><span data-stu-id="b5980-103">Removes a user on a device.</span></span>

## <span data-ttu-id="b5980-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5980-104">SYNTAX</span></span>

### <span data-ttu-id="b5980-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b5980-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5980-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5980-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5980-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5980-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5980-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5980-108">DESCRIPTION</span></span>
<span data-ttu-id="b5980-109">Cmdleten **Remove-AzDataBoxEdgeUser** tar bort en användare i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="b5980-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="b5980-110">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="b5980-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="b5980-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5980-111">EXAMPLES</span></span>

### <span data-ttu-id="b5980-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5980-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="b5980-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5980-113">PARAMETERS</span></span>

### <span data-ttu-id="b5980-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5980-114">-AsJob</span></span>
<span data-ttu-id="b5980-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b5980-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5980-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5980-116">-DefaultProfile</span></span>
<span data-ttu-id="b5980-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5980-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5980-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="b5980-118">-DeviceName</span></span>
<span data-ttu-id="b5980-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="b5980-119">Device Name</span></span>

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

### <span data-ttu-id="b5980-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5980-120">-InputObject</span></span>
<span data-ttu-id="b5980-121">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="b5980-121">Input Object</span></span>

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

### <span data-ttu-id="b5980-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5980-122">-Name</span></span>
<span data-ttu-id="b5980-123">Namnen</span><span class="sxs-lookup"><span data-stu-id="b5980-123">Username</span></span>

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

### <span data-ttu-id="b5980-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5980-124">-PassThru</span></span>
<span data-ttu-id="b5980-125">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="b5980-125">returns true if successful</span></span>

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

### <span data-ttu-id="b5980-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5980-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5980-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b5980-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b5980-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5980-128">-ResourceId</span></span>
<span data-ttu-id="b5980-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5980-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b5980-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5980-130">-Confirm</span></span>
<span data-ttu-id="b5980-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5980-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5980-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5980-132">-WhatIf</span></span>
<span data-ttu-id="b5980-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5980-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5980-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5980-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5980-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5980-135">CommonParameters</span></span>
<span data-ttu-id="b5980-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5980-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5980-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5980-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5980-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5980-138">INPUTS</span></span>

### <span data-ttu-id="b5980-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b5980-139">System.String</span></span>

### <span data-ttu-id="b5980-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b5980-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="b5980-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5980-141">OUTPUTS</span></span>

### <span data-ttu-id="b5980-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b5980-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="b5980-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5980-143">NOTES</span></span>

## <span data-ttu-id="b5980-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5980-144">RELATED LINKS</span></span>
