---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091633"
---
# <span data-ttu-id="a5922-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a5922-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a5922-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5922-102">SYNOPSIS</span></span>
<span data-ttu-id="a5922-103">Tar bort en autentiseringsuppgift för lagrings konton för en enhet.</span><span class="sxs-lookup"><span data-stu-id="a5922-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="a5922-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5922-104">SYNTAX</span></span>

### <span data-ttu-id="a5922-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a5922-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5922-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5922-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5922-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5922-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5922-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5922-108">DESCRIPTION</span></span>
<span data-ttu-id="a5922-109">Cmdleten **Remove-AzStackEdgeStorageAccountCredential** tar bort autentiseringsuppgifterna för lagrings kontot för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="a5922-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="a5922-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5922-110">EXAMPLES</span></span>

### <span data-ttu-id="a5922-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5922-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="a5922-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5922-112">PARAMETERS</span></span>

### <span data-ttu-id="a5922-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5922-113">-AsJob</span></span>
<span data-ttu-id="a5922-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a5922-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5922-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5922-115">-DefaultProfile</span></span>
<span data-ttu-id="a5922-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5922-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5922-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="a5922-117">-DeviceName</span></span>
<span data-ttu-id="a5922-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="a5922-118">Device Name</span></span>

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

### <span data-ttu-id="a5922-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5922-119">-InputObject</span></span>
<span data-ttu-id="a5922-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="a5922-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5922-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5922-121">-Name</span></span>
<span data-ttu-id="a5922-122">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="a5922-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5922-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5922-123">-PassThru</span></span>
<span data-ttu-id="a5922-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="a5922-124">returns true if successful</span></span>

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

### <span data-ttu-id="a5922-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5922-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5922-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a5922-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a5922-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5922-127">-ResourceId</span></span>
<span data-ttu-id="a5922-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5922-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a5922-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5922-129">-Confirm</span></span>
<span data-ttu-id="a5922-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5922-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5922-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5922-131">-WhatIf</span></span>
<span data-ttu-id="a5922-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5922-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5922-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5922-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5922-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5922-134">CommonParameters</span></span>
<span data-ttu-id="a5922-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5922-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5922-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5922-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5922-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5922-137">INPUTS</span></span>

### <span data-ttu-id="a5922-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a5922-138">System.String</span></span>

### <span data-ttu-id="a5922-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a5922-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a5922-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5922-140">OUTPUTS</span></span>

### <span data-ttu-id="a5922-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5922-141">System.Boolean</span></span>

## <span data-ttu-id="a5922-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5922-142">NOTES</span></span>

## <span data-ttu-id="a5922-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5922-143">RELATED LINKS</span></span>
