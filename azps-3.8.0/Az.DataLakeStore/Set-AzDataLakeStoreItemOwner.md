---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092751"
---
# <span data-ttu-id="eedbf-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="eedbf-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="eedbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eedbf-102">SYNOPSIS</span></span>
<span data-ttu-id="eedbf-103">Ändrar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eedbf-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="eedbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eedbf-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eedbf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eedbf-105">DESCRIPTION</span></span>
<span data-ttu-id="eedbf-106">Cmdleten **set-AzDataLakeStoreItemOwner** ändrar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="eedbf-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="eedbf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eedbf-107">EXAMPLES</span></span>

### <span data-ttu-id="eedbf-108">Exempel 1: ange ägare för ett objekt</span><span class="sxs-lookup"><span data-stu-id="eedbf-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="eedbf-109">Det här kommandot ställer in rot katalogen på Patti Nilsson.</span><span class="sxs-lookup"><span data-stu-id="eedbf-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="eedbf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eedbf-110">PARAMETERS</span></span>

### <span data-ttu-id="eedbf-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="eedbf-111">-Account</span></span>
<span data-ttu-id="eedbf-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="eedbf-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedbf-113">-DefaultProfile</span></span>
<span data-ttu-id="eedbf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eedbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eedbf-115">-ID</span><span class="sxs-lookup"><span data-stu-id="eedbf-115">-Id</span></span>
<span data-ttu-id="eedbf-116">Anger objekt-ID: t för AzureActive katalog användare, grupp eller tjänstens huvud namn som ska användas som ägare.</span><span class="sxs-lookup"><span data-stu-id="eedbf-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eedbf-117">-PassThru</span></span>
<span data-ttu-id="eedbf-118">Anger att den resulterande uppdaterade ägaren ska returneras.</span><span class="sxs-lookup"><span data-stu-id="eedbf-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-119">-Path</span><span class="sxs-lookup"><span data-stu-id="eedbf-119">-Path</span></span>
<span data-ttu-id="eedbf-120">Anger data Lake Store-sökvägen för det objekt som ska ändras, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="eedbf-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="eedbf-121">-Type</span></span>
<span data-ttu-id="eedbf-122">Anger typen av ägare som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="eedbf-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="eedbf-123">De acceptabla värdena för denna parameter är: User och Group.</span><span class="sxs-lookup"><span data-stu-id="eedbf-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eedbf-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eedbf-124">-Confirm</span></span>
<span data-ttu-id="eedbf-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eedbf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eedbf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eedbf-126">-WhatIf</span></span>
<span data-ttu-id="eedbf-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eedbf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eedbf-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eedbf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eedbf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedbf-129">CommonParameters</span></span>
<span data-ttu-id="eedbf-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eedbf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedbf-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eedbf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedbf-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eedbf-132">INPUTS</span></span>

### <span data-ttu-id="eedbf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eedbf-133">System.String</span></span>

### <span data-ttu-id="eedbf-134">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="eedbf-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="eedbf-135">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="eedbf-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="eedbf-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="eedbf-136">System.Guid</span></span>

### <span data-ttu-id="eedbf-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eedbf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eedbf-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eedbf-138">OUTPUTS</span></span>

### <span data-ttu-id="eedbf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eedbf-139">System.String</span></span>

## <span data-ttu-id="eedbf-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eedbf-140">NOTES</span></span>

## <span data-ttu-id="eedbf-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eedbf-141">RELATED LINKS</span></span>

[<span data-ttu-id="eedbf-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="eedbf-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


