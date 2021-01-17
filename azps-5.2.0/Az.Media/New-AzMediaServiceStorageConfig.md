---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: d53edc73bb1813841403348919758f1c6c13eff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398987"
---
# <span data-ttu-id="74e41-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="74e41-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="74e41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74e41-102">SYNOPSIS</span></span>
<span data-ttu-id="74e41-103">Skapa en lagrings konto konfiguration för medie tjänstens cmdletar.</span><span class="sxs-lookup"><span data-stu-id="74e41-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="74e41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74e41-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74e41-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74e41-105">DESCRIPTION</span></span>
<span data-ttu-id="74e41-106">Cmdleten **New-AzMediaServiceStorageConfig** skapar en lagrings konto konfiguration för medie tjänstens cmdletar.</span><span class="sxs-lookup"><span data-stu-id="74e41-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="74e41-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74e41-107">EXAMPLES</span></span>

### <span data-ttu-id="74e41-108">Exempel 1: skapa en lagrings konto konfiguration för medie tjänstens cmdletar</span><span class="sxs-lookup"><span data-stu-id="74e41-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="74e41-109">Det första kommandot skapar ett lagrings konto objekt genom att använda cmdlet **New-AzStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="74e41-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="74e41-110">Kommandot namnger detta lagrings konto Storage1 och typen heter Standard_GRS och lagrar resultatet i variabeln som heter $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="74e41-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="74e41-111">Det andra kommandot skapar ett Storage-konfigurationsobjekt som det primära lagrings kontot som är kopplat till medie tjänsten med hjälp av lagrings konto information som lagras i $StorageAccount variabeln.</span><span class="sxs-lookup"><span data-stu-id="74e41-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="74e41-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74e41-112">PARAMETERS</span></span>

### <span data-ttu-id="74e41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e41-113">-DefaultProfile</span></span>
<span data-ttu-id="74e41-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="74e41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74e41-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="74e41-115">-IsPrimary</span></span>
<span data-ttu-id="74e41-116">Anger att cmdleten skapar lagrings kontot som primär lagring för medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="74e41-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e41-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="74e41-117">-StorageAccountId</span></span>
<span data-ttu-id="74e41-118">Anger ID för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="74e41-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="74e41-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74e41-119">-Confirm</span></span>
<span data-ttu-id="74e41-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74e41-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e41-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e41-121">-WhatIf</span></span>
<span data-ttu-id="74e41-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74e41-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74e41-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74e41-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e41-124">CommonParameters</span></span>
<span data-ttu-id="74e41-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e41-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e41-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e41-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74e41-127">INPUTS</span></span>

### <span data-ttu-id="74e41-128">System. String</span><span class="sxs-lookup"><span data-stu-id="74e41-128">System.String</span></span>

## <span data-ttu-id="74e41-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74e41-129">OUTPUTS</span></span>

### <span data-ttu-id="74e41-130">Microsoft. Azure. commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74e41-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="74e41-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74e41-131">NOTES</span></span>

## <span data-ttu-id="74e41-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74e41-132">RELATED LINKS</span></span>

[<span data-ttu-id="74e41-133">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="74e41-133">Sync-AzMediaServiceStorageKey</span></span>](./Sync-AzMediaServiceStorageKey.md)


