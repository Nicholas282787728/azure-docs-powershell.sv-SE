---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: f211579d98957f48a389ad10c6044c6193ad9993
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744449"
---
# <span data-ttu-id="c4cdd-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="c4cdd-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="c4cdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cdd-103">Hämtar information om synkroniseringsinställningarna för en resurs.</span><span class="sxs-lookup"><span data-stu-id="c4cdd-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="c4cdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4cdd-104">SYNTAX</span></span>

### <span data-ttu-id="c4cdd-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4cdd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4cdd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4cdd-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4cdd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4cdd-107">DESCRIPTION</span></span>
<span data-ttu-id="c4cdd-108">Cmdleten **Get-AzDataShareSynchronization** innehåller information om alla synkroniseringsinställningar i en resurs under ett data delnings konto.</span><span class="sxs-lookup"><span data-stu-id="c4cdd-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="c4cdd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4cdd-109">EXAMPLES</span></span>

### <span data-ttu-id="c4cdd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4cdd-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="c4cdd-111">Det här kommandot innehåller information om alla synkroniseringsinställningar i dela AdsShare i WikiAds för data delning.</span><span class="sxs-lookup"><span data-stu-id="c4cdd-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="c4cdd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4cdd-112">PARAMETERS</span></span>

### <span data-ttu-id="c4cdd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4cdd-113">-AccountName</span></span>
<span data-ttu-id="c4cdd-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="c4cdd-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4cdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cdd-115">-DefaultProfile</span></span>
<span data-ttu-id="c4cdd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4cdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4cdd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4cdd-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4cdd-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="c4cdd-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4cdd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4cdd-119">-ResourceId</span></span>
<span data-ttu-id="c4cdd-120">Azure Data Share Resource-ID</span><span class="sxs-lookup"><span data-stu-id="c4cdd-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4cdd-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c4cdd-121">-ShareName</span></span>
<span data-ttu-id="c4cdd-122">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="c4cdd-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4cdd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cdd-123">CommonParameters</span></span>
<span data-ttu-id="c4cdd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4cdd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cdd-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cdd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cdd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4cdd-126">INPUTS</span></span>

### <span data-ttu-id="c4cdd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c4cdd-127">System.String</span></span>

## <span data-ttu-id="c4cdd-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4cdd-128">OUTPUTS</span></span>

### <span data-ttu-id="c4cdd-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="c4cdd-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="c4cdd-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4cdd-130">NOTES</span></span>

## <span data-ttu-id="c4cdd-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4cdd-131">RELATED LINKS</span></span>