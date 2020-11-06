---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 4e21d122c8a49209a7591457c36ba99fcc10496c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574296"
---
# <span data-ttu-id="45cb8-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45cb8-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="45cb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="45cb8-103">Tar bort ett data Lake Store-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="45cb8-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45cb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45cb8-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45cb8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="45cb8-106">Cmdleten **Remove-AzureRmDataLakeStoreAccount** tar bort ett data Lake Store-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="45cb8-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="45cb8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="45cb8-108">Exempel 1: ta bort ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="45cb8-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="45cb8-109">Det här kommandot tar bort kontot som heter ContosoADL från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="45cb8-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="45cb8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45cb8-110">PARAMETERS</span></span>

### <span data-ttu-id="45cb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45cb8-111">-DefaultProfile</span></span>
<span data-ttu-id="45cb8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="45cb8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="45cb8-113">-Force</span></span>
<span data-ttu-id="45cb8-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="45cb8-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="45cb8-115">-Name</span></span>
<span data-ttu-id="45cb8-116">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="45cb8-116">Specifies the name of the account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45cb8-117">-PassThru</span></span>
<span data-ttu-id="45cb8-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="45cb8-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45cb8-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="45cb8-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45cb8-120">-ResourceGroupName</span></span>
<span data-ttu-id="45cb8-121">Anger den resurs grupp som innehåller kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="45cb8-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45cb8-122">-Confirm</span></span>
<span data-ttu-id="45cb8-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45cb8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45cb8-124">-WhatIf</span></span>
<span data-ttu-id="45cb8-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45cb8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45cb8-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45cb8-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cb8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45cb8-127">CommonParameters</span></span>
<span data-ttu-id="45cb8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45cb8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45cb8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45cb8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45cb8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45cb8-130">INPUTS</span></span>

### <span data-ttu-id="45cb8-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="45cb8-131">None</span></span>
<span data-ttu-id="45cb8-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="45cb8-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45cb8-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45cb8-133">OUTPUTS</span></span>

### <span data-ttu-id="45cb8-134">bool</span><span class="sxs-lookup"><span data-stu-id="45cb8-134">bool</span></span>
<span data-ttu-id="45cb8-135">Om PassThru är angivet returneras sant när du är klar.</span><span class="sxs-lookup"><span data-stu-id="45cb8-135">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="45cb8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45cb8-136">NOTES</span></span>

## <span data-ttu-id="45cb8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45cb8-137">RELATED LINKS</span></span>

[<span data-ttu-id="45cb8-138">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45cb8-138">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="45cb8-139">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45cb8-139">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="45cb8-140">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45cb8-140">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="45cb8-141">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="45cb8-141">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


