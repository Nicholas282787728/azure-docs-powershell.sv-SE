---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260477"
---
# <span data-ttu-id="ce55b-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="ce55b-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="ce55b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce55b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce55b-103">Returnerar BitLocker-nycklarna för alla enheter i det angivna jobbet.</span><span class="sxs-lookup"><span data-stu-id="ce55b-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="ce55b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce55b-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ce55b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce55b-105">DESCRIPTION</span></span>
<span data-ttu-id="ce55b-106">Returnerar BitLocker-nycklarna för alla enheter i det angivna jobbet.</span><span class="sxs-lookup"><span data-stu-id="ce55b-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="ce55b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce55b-107">EXAMPLES</span></span>

### <span data-ttu-id="ce55b-108">Exempel 1: Visa alla BitLocker-nycklar i angivet ImportExport-jobb</span><span class="sxs-lookup"><span data-stu-id="ce55b-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="ce55b-109">Denna cmdlet visar alla BitLocker-nycklar i angivet ImportExport-jobb.</span><span class="sxs-lookup"><span data-stu-id="ce55b-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="ce55b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce55b-110">PARAMETERS</span></span>

### <span data-ttu-id="ce55b-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ce55b-111">-AcceptLanguage</span></span>
<span data-ttu-id="ce55b-112">Anger önskat språk för svaret.</span><span class="sxs-lookup"><span data-stu-id="ce55b-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce55b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce55b-113">-DefaultProfile</span></span>
<span data-ttu-id="ce55b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce55b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce55b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce55b-115">-JobName</span></span>
<span data-ttu-id="ce55b-116">Namnet på import-och export jobbet.</span><span class="sxs-lookup"><span data-stu-id="ce55b-116">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce55b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce55b-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce55b-118">Resurs gruppens namn identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ce55b-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce55b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce55b-119">-SubscriptionId</span></span>
<span data-ttu-id="ce55b-120">Abonnemangs-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="ce55b-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce55b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce55b-121">CommonParameters</span></span>
<span data-ttu-id="ce55b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce55b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce55b-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce55b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce55b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce55b-124">INPUTS</span></span>

## <span data-ttu-id="ce55b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce55b-125">OUTPUTS</span></span>

### <span data-ttu-id="ce55b-126">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="ce55b-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="ce55b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce55b-127">NOTES</span></span>

<span data-ttu-id="ce55b-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ce55b-128">ALIASES</span></span>

## <span data-ttu-id="ce55b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce55b-129">RELATED LINKS</span></span>

