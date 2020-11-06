---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586536"
---
# <span data-ttu-id="03390-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="03390-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="03390-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03390-102">SYNOPSIS</span></span>
<span data-ttu-id="03390-103">Anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="03390-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03390-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03390-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03390-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03390-105">DESCRIPTION</span></span>
<span data-ttu-id="03390-106">Cmdleten **set-AzureRmDataLakeStoreItemExpiry** anger eller tar bort förfallo tiden för en fil i ett Azure Data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="03390-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="03390-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03390-107">EXAMPLES</span></span>

### <span data-ttu-id="03390-108">Exempel 1: Ange förfallo tid för en fil</span><span class="sxs-lookup"><span data-stu-id="03390-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="03390-109">Ställer in utgångs datum på filen myfile.txt i konto ContosoADL till två timmar från nu.</span><span class="sxs-lookup"><span data-stu-id="03390-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="03390-110">Detta gör att filen upphör att gälla (markeras för borttagning) om två timmar.</span><span class="sxs-lookup"><span data-stu-id="03390-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="03390-111">Exempel 2: ta bort utgångs datum för en fil</span><span class="sxs-lookup"><span data-stu-id="03390-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="03390-112">Tar bort eventuell utgångs datum som tidigare ställts in på filen myfile.txt i kontot ' ContosoADL '.</span><span class="sxs-lookup"><span data-stu-id="03390-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="03390-113">Det innebär att filen inte automatiskt upphör att gälla (markeras för borttagning) och måste tas bort manuellt eller ställas in på nytt.</span><span class="sxs-lookup"><span data-stu-id="03390-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="03390-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03390-114">PARAMETERS</span></span>

### <span data-ttu-id="03390-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="03390-115">-Account</span></span>
<span data-ttu-id="03390-116">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="03390-116">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="03390-117">-Utgång</span><span class="sxs-lookup"><span data-stu-id="03390-117">-Expiration</span></span>
<span data-ttu-id="03390-118">Den absoluta förfallo tiden för den angivna filen.</span><span class="sxs-lookup"><span data-stu-id="03390-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="03390-119">Om det inte finns något värde eller angett till MaxValue upphör filen aldrig att gälla.</span><span class="sxs-lookup"><span data-stu-id="03390-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03390-120">-Path</span><span class="sxs-lookup"><span data-stu-id="03390-120">-Path</span></span>
<span data-ttu-id="03390-121">Anger data Lake Store-sökvägen för det fil objekt för vilket du vill ange eller ta bort förfallo datum.</span><span class="sxs-lookup"><span data-stu-id="03390-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="03390-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03390-122">-Confirm</span></span>
<span data-ttu-id="03390-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03390-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03390-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03390-124">-WhatIf</span></span>
<span data-ttu-id="03390-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03390-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03390-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03390-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03390-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03390-127">-DefaultProfile</span></span>
<span data-ttu-id="03390-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03390-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03390-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03390-129">CommonParameters</span></span>
<span data-ttu-id="03390-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03390-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03390-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03390-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03390-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03390-132">INPUTS</span></span>

## <span data-ttu-id="03390-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03390-133">OUTPUTS</span></span>

### <span data-ttu-id="03390-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03390-134">DataLakeStoreItem</span></span>
<span data-ttu-id="03390-135">Den uppdaterade filen med en ny förfallo tid.</span><span class="sxs-lookup"><span data-stu-id="03390-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="03390-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03390-136">NOTES</span></span>
<span data-ttu-id="03390-137">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="03390-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="03390-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03390-138">RELATED LINKS</span></span>

[<span data-ttu-id="03390-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03390-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

