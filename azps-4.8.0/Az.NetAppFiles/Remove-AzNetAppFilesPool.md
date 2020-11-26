---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103157"
---
# <span data-ttu-id="5c67e-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5c67e-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="5c67e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c67e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c67e-103">Tar bort en ANF-pool (Azure NetApp-filer).</span><span class="sxs-lookup"><span data-stu-id="5c67e-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="5c67e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c67e-104">SYNTAX</span></span>

### <span data-ttu-id="5c67e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5c67e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c67e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c67e-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c67e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c67e-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c67e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c67e-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c67e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c67e-109">DESCRIPTION</span></span>
<span data-ttu-id="5c67e-110">Cmdleten **Remove-AzNetAppFilesPool** tar bort en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="5c67e-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="5c67e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c67e-111">EXAMPLES</span></span>

### <span data-ttu-id="5c67e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c67e-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="5c67e-113">Det här kommandot tar bort ANF-poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="5c67e-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="5c67e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c67e-114">PARAMETERS</span></span>

### <span data-ttu-id="5c67e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c67e-115">-AccountName</span></span>
<span data-ttu-id="5c67e-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="5c67e-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c67e-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5c67e-117">-AccountObject</span></span>
<span data-ttu-id="5c67e-118">Det konto objekt som innehåller poolen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="5c67e-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c67e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c67e-119">-DefaultProfile</span></span>
<span data-ttu-id="5c67e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c67e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c67e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c67e-121">-InputObject</span></span>
<span data-ttu-id="5c67e-122">Pool-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="5c67e-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c67e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c67e-123">-Name</span></span>
<span data-ttu-id="5c67e-124">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5c67e-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c67e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c67e-125">-PassThru</span></span>
<span data-ttu-id="5c67e-126">Returnera om den angivna poolen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="5c67e-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="5c67e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c67e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c67e-128">ANF resurs grupp</span><span class="sxs-lookup"><span data-stu-id="5c67e-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c67e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c67e-129">-ResourceId</span></span>
<span data-ttu-id="5c67e-130">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="5c67e-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c67e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c67e-131">-Confirm</span></span>
<span data-ttu-id="5c67e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c67e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c67e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c67e-133">-WhatIf</span></span>
<span data-ttu-id="5c67e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c67e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c67e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c67e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c67e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c67e-136">CommonParameters</span></span>
<span data-ttu-id="5c67e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c67e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c67e-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c67e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c67e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c67e-139">INPUTS</span></span>

### <span data-ttu-id="5c67e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5c67e-140">System.String</span></span>

### <span data-ttu-id="5c67e-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5c67e-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="5c67e-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5c67e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5c67e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c67e-143">OUTPUTS</span></span>

### <span data-ttu-id="5c67e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c67e-144">System.Boolean</span></span>

## <span data-ttu-id="5c67e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c67e-145">NOTES</span></span>

## <span data-ttu-id="5c67e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c67e-146">RELATED LINKS</span></span>