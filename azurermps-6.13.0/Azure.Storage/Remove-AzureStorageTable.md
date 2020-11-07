---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: a4083920e935077658d218663e0a0255f6566ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756049"
---
# <span data-ttu-id="08824-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="08824-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="08824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08824-102">SYNOPSIS</span></span>
<span data-ttu-id="08824-103">Tar bort en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="08824-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08824-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08824-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08824-105">DESCRIPTION</span></span>
<span data-ttu-id="08824-106">Cmdleten **Remove-AzureStorageTable** tar bort en eller flera lagrings tabeller från ett lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="08824-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="08824-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08824-107">EXAMPLES</span></span>

### <span data-ttu-id="08824-108">Exempel 1: ta bort en tabell</span><span class="sxs-lookup"><span data-stu-id="08824-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="08824-109">Det här kommandot tar bort en tabell.</span><span class="sxs-lookup"><span data-stu-id="08824-109">This command removes a table.</span></span>

### <span data-ttu-id="08824-110">Exempel 2: ta bort flera tabeller</span><span class="sxs-lookup"><span data-stu-id="08824-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="08824-111">I det här exemplet används ett jokertecken med parametern *Name* för att hämta alla tabeller som matchar tabellen mönster och sedan skickas resultatet i pipeline för att ta bort tabellerna.</span><span class="sxs-lookup"><span data-stu-id="08824-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="08824-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08824-112">PARAMETERS</span></span>

### <span data-ttu-id="08824-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="08824-113">-Context</span></span>
<span data-ttu-id="08824-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="08824-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="08824-115">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08824-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="08824-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08824-116">-DefaultProfile</span></span>
<span data-ttu-id="08824-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08824-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08824-118">-Force</span><span class="sxs-lookup"><span data-stu-id="08824-118">-Force</span></span>
<span data-ttu-id="08824-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="08824-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08824-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="08824-120">-Name</span></span>
<span data-ttu-id="08824-121">Anger namnet på tabellen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="08824-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08824-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08824-122">-PassThru</span></span>
<span data-ttu-id="08824-123">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="08824-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="08824-124">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="08824-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="08824-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08824-125">-Confirm</span></span>
<span data-ttu-id="08824-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08824-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08824-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08824-127">-WhatIf</span></span>
<span data-ttu-id="08824-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08824-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08824-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08824-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08824-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08824-130">CommonParameters</span></span>
<span data-ttu-id="08824-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08824-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08824-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08824-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08824-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08824-133">INPUTS</span></span>

### <span data-ttu-id="08824-134">System. String</span><span class="sxs-lookup"><span data-stu-id="08824-134">System.String</span></span>

### <span data-ttu-id="08824-135">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="08824-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="08824-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08824-136">OUTPUTS</span></span>

### <span data-ttu-id="08824-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08824-137">System.Boolean</span></span>

## <span data-ttu-id="08824-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08824-138">NOTES</span></span>

## <span data-ttu-id="08824-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08824-139">RELATED LINKS</span></span>

[<span data-ttu-id="08824-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="08824-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
