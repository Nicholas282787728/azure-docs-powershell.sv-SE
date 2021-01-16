---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521994"
---
# <span data-ttu-id="2e6ca-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6ca-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="2e6ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6ca-103">Tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="2e6ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e6ca-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e6ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e6ca-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6ca-106">Cmdleten **Remove-AzStorageTableStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="2e6ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e6ca-107">EXAMPLES</span></span>

### <span data-ttu-id="2e6ca-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="2e6ca-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="2e6ca-109">Det här kommandot tar bort principen med namnet Policy05 från lagrings tabellen tabell.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="2e6ca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e6ca-110">PARAMETERS</span></span>

### <span data-ttu-id="2e6ca-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2e6ca-111">-Context</span></span>
<span data-ttu-id="2e6ca-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2e6ca-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6ca-114">-DefaultProfile</span></span>
<span data-ttu-id="2e6ca-115">kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-115">communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6ca-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e6ca-116">-PassThru</span></span>
<span data-ttu-id="2e6ca-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2e6ca-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2e6ca-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="2e6ca-119">-Policy</span></span>
<span data-ttu-id="2e6ca-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6ca-121">-Tabell</span><span class="sxs-lookup"><span data-stu-id="2e6ca-121">-Table</span></span>
<span data-ttu-id="2e6ca-122">Anger namnet på Azure-tabellen.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6ca-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e6ca-123">-Confirm</span></span>
<span data-ttu-id="2e6ca-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6ca-125">-WhatIf</span></span>
<span data-ttu-id="2e6ca-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e6ca-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6ca-128">CommonParameters</span></span>
<span data-ttu-id="2e6ca-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6ca-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6ca-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6ca-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e6ca-131">INPUTS</span></span>

### <span data-ttu-id="2e6ca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6ca-132">System.String</span></span>

### <span data-ttu-id="2e6ca-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e6ca-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2e6ca-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e6ca-134">OUTPUTS</span></span>

### <span data-ttu-id="2e6ca-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e6ca-135">System.Boolean</span></span>

## <span data-ttu-id="2e6ca-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e6ca-136">NOTES</span></span>

## <span data-ttu-id="2e6ca-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e6ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e6ca-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6ca-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2e6ca-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e6ca-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2e6ca-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6ca-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2e6ca-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6ca-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
