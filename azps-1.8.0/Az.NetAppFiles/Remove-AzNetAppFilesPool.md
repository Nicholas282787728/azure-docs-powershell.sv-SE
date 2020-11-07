---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753994"
---
# <span data-ttu-id="860e7-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="860e7-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="860e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="860e7-102">SYNOPSIS</span></span>
<span data-ttu-id="860e7-103">Tar bort en ANF-pool (Azure NetApp-filer).</span><span class="sxs-lookup"><span data-stu-id="860e7-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="860e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="860e7-104">SYNTAX</span></span>

### <span data-ttu-id="860e7-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="860e7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="860e7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="860e7-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="860e7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="860e7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="860e7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="860e7-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="860e7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="860e7-109">DESCRIPTION</span></span>
<span data-ttu-id="860e7-110">Cmdleten **Remove-AzNetAppFilesPool** tar bort en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="860e7-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="860e7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="860e7-111">EXAMPLES</span></span>

### <span data-ttu-id="860e7-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="860e7-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="860e7-113">Det här kommandot tar bort ANF-poolen "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="860e7-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="860e7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="860e7-114">PARAMETERS</span></span>

### <span data-ttu-id="860e7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="860e7-115">-AccountName</span></span>
<span data-ttu-id="860e7-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="860e7-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="860e7-117">-AccountObject</span></span>
<span data-ttu-id="860e7-118">Det konto objekt som innehåller poolen som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="860e7-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860e7-119">-DefaultProfile</span></span>
<span data-ttu-id="860e7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="860e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="860e7-121">-InputObject</span></span>
<span data-ttu-id="860e7-122">Pool-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="860e7-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="860e7-123">-Name</span></span>
<span data-ttu-id="860e7-124">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="860e7-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="860e7-125">-PassThru</span></span>
<span data-ttu-id="860e7-126">Returnera om den angivna poolen har tagits bort</span><span class="sxs-lookup"><span data-stu-id="860e7-126">Return whether the specified pool was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="860e7-128">ANF resurs grupp</span><span class="sxs-lookup"><span data-stu-id="860e7-128">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="860e7-129">-ResourceId</span></span>
<span data-ttu-id="860e7-130">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="860e7-130">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="860e7-131">-Confirm</span></span>
<span data-ttu-id="860e7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="860e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="860e7-133">-WhatIf</span></span>
<span data-ttu-id="860e7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="860e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="860e7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="860e7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860e7-136">CommonParameters</span></span>
<span data-ttu-id="860e7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="860e7-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860e7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860e7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="860e7-139">INPUTS</span></span>

### <span data-ttu-id="860e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="860e7-140">System.String</span></span>

### <span data-ttu-id="860e7-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="860e7-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="860e7-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="860e7-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="860e7-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="860e7-143">OUTPUTS</span></span>

### <span data-ttu-id="860e7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="860e7-144">System.Boolean</span></span>

## <span data-ttu-id="860e7-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="860e7-145">NOTES</span></span>

## <span data-ttu-id="860e7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="860e7-146">RELATED LINKS</span></span>
