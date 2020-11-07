---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6d32ddf53f675f2ab2897e4bb9ec85655e0fcd14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931066"
---
# <span data-ttu-id="66bad-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66bad-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="66bad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66bad-102">SYNOPSIS</span></span>
<span data-ttu-id="66bad-103">Tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="66bad-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66bad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66bad-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66bad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66bad-105">DESCRIPTION</span></span>
<span data-ttu-id="66bad-106">Cmdleten **Remove-AzureStorageTableStoredAccessPolicy** tar bort en lagrad åtkomst princip från en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="66bad-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="66bad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66bad-107">EXAMPLES</span></span>

### <span data-ttu-id="66bad-108">Exempel 1: ta bort en lagrad åtkomst princip från en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="66bad-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="66bad-109">Det här kommandot tar bort principen med namnet Policy05 från lagrings tabellen tabell.</span><span class="sxs-lookup"><span data-stu-id="66bad-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="66bad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66bad-110">PARAMETERS</span></span>

### <span data-ttu-id="66bad-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="66bad-111">-Context</span></span>
<span data-ttu-id="66bad-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="66bad-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="66bad-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="66bad-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="66bad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bad-114">-DefaultProfile</span></span>
<span data-ttu-id="66bad-115">kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66bad-115">communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bad-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66bad-116">-PassThru</span></span>
<span data-ttu-id="66bad-117">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="66bad-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="66bad-118">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="66bad-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="66bad-119">-Princip</span><span class="sxs-lookup"><span data-stu-id="66bad-119">-Policy</span></span>
<span data-ttu-id="66bad-120">Anger namnet på den lagrade åtkomst principen som tas bort av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66bad-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66bad-121">-Tabell</span><span class="sxs-lookup"><span data-stu-id="66bad-121">-Table</span></span>
<span data-ttu-id="66bad-122">Anger namnet på Azure-tabellen.</span><span class="sxs-lookup"><span data-stu-id="66bad-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="66bad-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66bad-123">-Confirm</span></span>
<span data-ttu-id="66bad-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66bad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bad-125">-WhatIf</span></span>
<span data-ttu-id="66bad-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66bad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66bad-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66bad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bad-128">CommonParameters</span></span>
<span data-ttu-id="66bad-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bad-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bad-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66bad-131">INPUTS</span></span>

### <span data-ttu-id="66bad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="66bad-132">System.String</span></span>

### <span data-ttu-id="66bad-133">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="66bad-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66bad-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66bad-134">OUTPUTS</span></span>

### <span data-ttu-id="66bad-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66bad-135">System.Boolean</span></span>

## <span data-ttu-id="66bad-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66bad-136">NOTES</span></span>

## <span data-ttu-id="66bad-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66bad-137">RELATED LINKS</span></span>

[<span data-ttu-id="66bad-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66bad-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="66bad-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="66bad-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="66bad-140">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66bad-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="66bad-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66bad-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
