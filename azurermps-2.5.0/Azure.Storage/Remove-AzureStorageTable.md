---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: e33e32051c15483956d0764f5e9ddca25a083f23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931069"
---
# <span data-ttu-id="72002-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="72002-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="72002-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72002-102">SYNOPSIS</span></span>
<span data-ttu-id="72002-103">Tar bort en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="72002-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72002-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72002-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72002-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72002-105">DESCRIPTION</span></span>
<span data-ttu-id="72002-106">Cmdleten **Remove-AzureStorageTable** tar bort en eller flera lagrings tabeller från ett lagrings konto i Azure.</span><span class="sxs-lookup"><span data-stu-id="72002-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="72002-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72002-107">EXAMPLES</span></span>

### <span data-ttu-id="72002-108">Exempel 1: ta bort en tabell</span><span class="sxs-lookup"><span data-stu-id="72002-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="72002-109">Det här kommandot tar bort en tabell.</span><span class="sxs-lookup"><span data-stu-id="72002-109">This command removes a table.</span></span>

### <span data-ttu-id="72002-110">Exempel 2: ta bort flera tabeller</span><span class="sxs-lookup"><span data-stu-id="72002-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="72002-111">I det här exemplet används ett jokertecken med parametern *Name* för att hämta alla tabeller som matchar tabellen mönster och sedan skickas resultatet i pipeline för att ta bort tabellerna.</span><span class="sxs-lookup"><span data-stu-id="72002-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="72002-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72002-112">PARAMETERS</span></span>

### <span data-ttu-id="72002-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="72002-113">-Context</span></span>
<span data-ttu-id="72002-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="72002-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="72002-115">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72002-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="72002-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72002-116">-DefaultProfile</span></span>
<span data-ttu-id="72002-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72002-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72002-118">-Force</span><span class="sxs-lookup"><span data-stu-id="72002-118">-Force</span></span>
<span data-ttu-id="72002-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="72002-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72002-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="72002-120">-Name</span></span>
<span data-ttu-id="72002-121">Anger namnet på tabellen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72002-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="72002-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72002-122">-PassThru</span></span>
<span data-ttu-id="72002-123">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="72002-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="72002-124">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="72002-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="72002-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72002-125">-Confirm</span></span>
<span data-ttu-id="72002-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72002-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72002-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72002-127">-WhatIf</span></span>
<span data-ttu-id="72002-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72002-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72002-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72002-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72002-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72002-130">CommonParameters</span></span>
<span data-ttu-id="72002-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72002-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72002-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72002-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72002-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72002-133">INPUTS</span></span>

### <span data-ttu-id="72002-134">System. String</span><span class="sxs-lookup"><span data-stu-id="72002-134">System.String</span></span>

### <span data-ttu-id="72002-135">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="72002-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72002-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72002-136">OUTPUTS</span></span>

### <span data-ttu-id="72002-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72002-137">System.Boolean</span></span>

## <span data-ttu-id="72002-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72002-138">NOTES</span></span>

## <span data-ttu-id="72002-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72002-139">RELATED LINKS</span></span>

[<span data-ttu-id="72002-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="72002-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
