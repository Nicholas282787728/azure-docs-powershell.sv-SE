---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580448"
---
# <span data-ttu-id="b58f6-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b58f6-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="b58f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b58f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b58f6-103">Ändrar behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b58f6-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b58f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b58f6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b58f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b58f6-105">DESCRIPTION</span></span>
<span data-ttu-id="b58f6-106">Cmdleten **set-AzureRmDataLakeStoreItemPermission** ändrar behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b58f6-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b58f6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b58f6-107">EXAMPLES</span></span>

### <span data-ttu-id="b58f6-108">Exempel 1: Ange behörigheten oktalt för ett objekt</span><span class="sxs-lookup"><span data-stu-id="b58f6-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="b58f6-109">Det här kommandot ställer in behörigheten oktalt för en fil till 0770, som översätter att rensa trögheten, ange behörigheterna läsa/skriva/köra för ägaren av filen, ange behörigheterna läsa/skriva/köra för den ägandede gruppen i filen och rensa behörigheterna läsa/skriva/köra för andra.</span><span class="sxs-lookup"><span data-stu-id="b58f6-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="b58f6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b58f6-110">PARAMETERS</span></span>

### <span data-ttu-id="b58f6-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b58f6-111">-Account</span></span>
<span data-ttu-id="b58f6-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="b58f6-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b58f6-113">-DefaultProfile</span></span>
<span data-ttu-id="b58f6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b58f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b58f6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b58f6-115">-Path</span></span>
<span data-ttu-id="b58f6-116">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="b58f6-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58f6-117">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="b58f6-117">-Permission</span></span>
<span data-ttu-id="b58f6-118">De behörigheter som ska anges för filen eller mappen, uttryckt som ett oktalt (till exempel "777")</span><span class="sxs-lookup"><span data-stu-id="b58f6-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b58f6-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b58f6-119">-Confirm</span></span>
<span data-ttu-id="b58f6-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b58f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b58f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b58f6-121">-WhatIf</span></span>
<span data-ttu-id="b58f6-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b58f6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b58f6-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b58f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b58f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b58f6-124">CommonParameters</span></span>
<span data-ttu-id="b58f6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b58f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b58f6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b58f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b58f6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b58f6-127">INPUTS</span></span>

### <span data-ttu-id="b58f6-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="b58f6-128">None</span></span>
<span data-ttu-id="b58f6-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b58f6-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b58f6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b58f6-130">OUTPUTS</span></span>

### <span data-ttu-id="b58f6-131">bool</span><span class="sxs-lookup"><span data-stu-id="b58f6-131">bool</span></span>
<span data-ttu-id="b58f6-132">Returnerar true när behörigheten har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="b58f6-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="b58f6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b58f6-133">NOTES</span></span>
* <span data-ttu-id="b58f6-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b58f6-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="b58f6-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b58f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="b58f6-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b58f6-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


