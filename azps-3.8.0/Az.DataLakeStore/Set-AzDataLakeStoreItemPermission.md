---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092747"
---
# <span data-ttu-id="90c15-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="90c15-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="90c15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90c15-102">SYNOPSIS</span></span>
<span data-ttu-id="90c15-103">Ändrar behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="90c15-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="90c15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90c15-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90c15-105">DESCRIPTION</span></span>
<span data-ttu-id="90c15-106">Cmdleten **set-AzDataLakeStoreItemPermission** ändrar behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="90c15-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="90c15-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90c15-107">EXAMPLES</span></span>

### <span data-ttu-id="90c15-108">Exempel 1: Ange behörigheten oktalt för ett objekt</span><span class="sxs-lookup"><span data-stu-id="90c15-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="90c15-109">Det här kommandot ställer in behörigheten oktalt för en fil till 0770, som översätter att rensa trögheten, ange behörigheterna läsa/skriva/köra för ägaren av filen, ange behörigheterna läsa/skriva/köra för den ägandede gruppen i filen och rensa behörigheterna läsa/skriva/köra för andra.</span><span class="sxs-lookup"><span data-stu-id="90c15-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="90c15-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90c15-110">PARAMETERS</span></span>

### <span data-ttu-id="90c15-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="90c15-111">-Account</span></span>
<span data-ttu-id="90c15-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="90c15-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="90c15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c15-113">-DefaultProfile</span></span>
<span data-ttu-id="90c15-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90c15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c15-115">-Path</span><span class="sxs-lookup"><span data-stu-id="90c15-115">-Path</span></span>
<span data-ttu-id="90c15-116">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="90c15-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="90c15-117">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="90c15-117">-Permission</span></span>
<span data-ttu-id="90c15-118">De behörigheter som ska anges för filen eller mappen, uttryckt som ett oktalt (till exempel "777")</span><span class="sxs-lookup"><span data-stu-id="90c15-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c15-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90c15-119">-Confirm</span></span>
<span data-ttu-id="90c15-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90c15-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c15-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c15-121">-WhatIf</span></span>
<span data-ttu-id="90c15-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90c15-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c15-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90c15-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c15-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c15-124">CommonParameters</span></span>
<span data-ttu-id="90c15-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c15-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c15-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c15-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c15-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90c15-127">INPUTS</span></span>

### <span data-ttu-id="90c15-128">System. String</span><span class="sxs-lookup"><span data-stu-id="90c15-128">System.String</span></span>

### <span data-ttu-id="90c15-129">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="90c15-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="90c15-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="90c15-130">System.Int32</span></span>

## <span data-ttu-id="90c15-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90c15-131">OUTPUTS</span></span>

### <span data-ttu-id="90c15-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90c15-132">System.Boolean</span></span>

## <span data-ttu-id="90c15-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90c15-133">NOTES</span></span>
* <span data-ttu-id="90c15-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="90c15-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="90c15-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90c15-135">RELATED LINKS</span></span>

[<span data-ttu-id="90c15-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="90c15-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


