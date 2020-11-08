---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260937"
---
# <span data-ttu-id="51c1d-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="51c1d-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="51c1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="51c1d-103">Tar bort en autentiseringsuppgift för lagrings konton för en enhet.</span><span class="sxs-lookup"><span data-stu-id="51c1d-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="51c1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51c1d-104">SYNTAX</span></span>

### <span data-ttu-id="51c1d-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51c1d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51c1d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51c1d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51c1d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51c1d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51c1d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51c1d-108">DESCRIPTION</span></span>
<span data-ttu-id="51c1d-109">Cmdleten **Remove-AzStackEdgeStorageAccountCredential** tar bort autentiseringsuppgifterna för lagrings kontot för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="51c1d-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="51c1d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51c1d-110">EXAMPLES</span></span>

### <span data-ttu-id="51c1d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51c1d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="51c1d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51c1d-112">PARAMETERS</span></span>

### <span data-ttu-id="51c1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51c1d-113">-AsJob</span></span>
<span data-ttu-id="51c1d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51c1d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51c1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c1d-115">-DefaultProfile</span></span>
<span data-ttu-id="51c1d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51c1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c1d-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="51c1d-117">-DeviceName</span></span>
<span data-ttu-id="51c1d-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="51c1d-118">Device Name</span></span>

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

### <span data-ttu-id="51c1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51c1d-119">-InputObject</span></span>
<span data-ttu-id="51c1d-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="51c1d-120">Input Object</span></span>

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

### <span data-ttu-id="51c1d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="51c1d-121">-Name</span></span>
<span data-ttu-id="51c1d-122">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="51c1d-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="51c1d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51c1d-123">-PassThru</span></span>
<span data-ttu-id="51c1d-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="51c1d-124">returns true if successful</span></span>

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

### <span data-ttu-id="51c1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51c1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="51c1d-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="51c1d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="51c1d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51c1d-127">-ResourceId</span></span>
<span data-ttu-id="51c1d-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="51c1d-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="51c1d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51c1d-129">-Confirm</span></span>
<span data-ttu-id="51c1d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51c1d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c1d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c1d-131">-WhatIf</span></span>
<span data-ttu-id="51c1d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51c1d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51c1d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51c1d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51c1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c1d-134">CommonParameters</span></span>
<span data-ttu-id="51c1d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c1d-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51c1d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c1d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51c1d-137">INPUTS</span></span>

### <span data-ttu-id="51c1d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="51c1d-138">System.String</span></span>

### <span data-ttu-id="51c1d-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="51c1d-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="51c1d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51c1d-140">OUTPUTS</span></span>

### <span data-ttu-id="51c1d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51c1d-141">System.Boolean</span></span>

## <span data-ttu-id="51c1d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51c1d-142">NOTES</span></span>

## <span data-ttu-id="51c1d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51c1d-143">RELATED LINKS</span></span>
