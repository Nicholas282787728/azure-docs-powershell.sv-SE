---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581439"
---
# <span data-ttu-id="167df-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="167df-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="167df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="167df-102">SYNOPSIS</span></span>
<span data-ttu-id="167df-103">Tar bort ett data Lake Store-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="167df-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="167df-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="167df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="167df-105">DESCRIPTION</span></span>
<span data-ttu-id="167df-106">Cmdleten **Remove-AzureRmDataLakeStoreAccount** tar bort ett data Lake Store-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="167df-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="167df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="167df-107">EXAMPLES</span></span>

### <span data-ttu-id="167df-108">Exempel 1: ta bort ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="167df-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="167df-109">Det här kommandot tar bort kontot som heter ContosoADL från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="167df-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="167df-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="167df-110">PARAMETERS</span></span>

### <span data-ttu-id="167df-111">-Force</span><span class="sxs-lookup"><span data-stu-id="167df-111">-Force</span></span>
<span data-ttu-id="167df-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="167df-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167df-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="167df-113">-Name</span></span>
<span data-ttu-id="167df-114">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="167df-114">Specifies the name of the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="167df-115">-PassThru</span></span>
<span data-ttu-id="167df-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="167df-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="167df-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="167df-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167df-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167df-118">-ResourceGroupName</span></span>
<span data-ttu-id="167df-119">Anger den resurs grupp som innehåller kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="167df-119">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="167df-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="167df-120">-Confirm</span></span>
<span data-ttu-id="167df-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="167df-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="167df-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="167df-122">-WhatIf</span></span>
<span data-ttu-id="167df-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="167df-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="167df-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="167df-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="167df-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167df-125">-DefaultProfile</span></span>
<span data-ttu-id="167df-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="167df-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="167df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167df-127">CommonParameters</span></span>
<span data-ttu-id="167df-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167df-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167df-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167df-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="167df-130">INPUTS</span></span>

## <span data-ttu-id="167df-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="167df-131">OUTPUTS</span></span>

### <span data-ttu-id="167df-132">bool</span><span class="sxs-lookup"><span data-stu-id="167df-132">bool</span></span>
<span data-ttu-id="167df-133">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="167df-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="167df-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="167df-134">NOTES</span></span>

## <span data-ttu-id="167df-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="167df-135">RELATED LINKS</span></span>

[<span data-ttu-id="167df-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="167df-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="167df-137">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="167df-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="167df-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="167df-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="167df-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="167df-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


