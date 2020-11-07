---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758411"
---
# <span data-ttu-id="8fa7d-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="8fa7d-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="8fa7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa7d-103">Ändrar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fa7d-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fa7d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fa7d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa7d-106">Cmdleten **set-AzureRmDataLakeStoreItemOwner** ändrar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8fa7d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fa7d-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa7d-108">Exempel 1: ange ägare för ett objekt</span><span class="sxs-lookup"><span data-stu-id="8fa7d-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="8fa7d-109">Det här kommandot ställer in rot katalogen på Patti Nilsson.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="8fa7d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fa7d-110">PARAMETERS</span></span>

### <span data-ttu-id="8fa7d-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8fa7d-111">-Account</span></span>
<span data-ttu-id="8fa7d-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8fa7d-113">-ID</span><span class="sxs-lookup"><span data-stu-id="8fa7d-113">-Id</span></span>
<span data-ttu-id="8fa7d-114">Anger objekt-ID: t för AzureActive katalog användare, grupp eller tjänstens huvud namn som ska användas som ägare.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="8fa7d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fa7d-115">-PassThru</span></span>
<span data-ttu-id="8fa7d-116">Anger att den resulterande uppdaterade ägaren ska returneras.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-116">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="8fa7d-117">-Path</span><span class="sxs-lookup"><span data-stu-id="8fa7d-117">-Path</span></span>
<span data-ttu-id="8fa7d-118">Anger data Lake Store-sökvägen för det objekt som ska ändras, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="8fa7d-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8fa7d-119">– Skriv</span><span class="sxs-lookup"><span data-stu-id="8fa7d-119">-Type</span></span>
<span data-ttu-id="8fa7d-120">Anger typen av ägare som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="8fa7d-121">De acceptabla värdena för denna parameter är: User och Group.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-121">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="8fa7d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fa7d-122">-Confirm</span></span>
<span data-ttu-id="8fa7d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa7d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa7d-124">-WhatIf</span></span>
<span data-ttu-id="8fa7d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fa7d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fa7d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa7d-127">-DefaultProfile</span></span>
<span data-ttu-id="8fa7d-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa7d-129">CommonParameters</span></span>
<span data-ttu-id="8fa7d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa7d-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa7d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa7d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fa7d-132">INPUTS</span></span>

## <span data-ttu-id="8fa7d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fa7d-133">OUTPUTS</span></span>

### <span data-ttu-id="8fa7d-134">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="8fa7d-134">string</span></span>
<span data-ttu-id="8fa7d-135">Om PassThru anges returnerar den uppdaterade ägaren.</span><span class="sxs-lookup"><span data-stu-id="8fa7d-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="8fa7d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fa7d-136">NOTES</span></span>

## <span data-ttu-id="8fa7d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fa7d-137">RELATED LINKS</span></span>

[<span data-ttu-id="8fa7d-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="8fa7d-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


