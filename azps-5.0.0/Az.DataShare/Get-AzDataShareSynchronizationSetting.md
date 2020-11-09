---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320323"
---
# <span data-ttu-id="78977-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="78977-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="78977-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78977-102">SYNOPSIS</span></span>
<span data-ttu-id="78977-103">Hämtar information om synkroniseringsinställningarna på en resurs.</span><span class="sxs-lookup"><span data-stu-id="78977-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="78977-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78977-104">SYNTAX</span></span>

### <span data-ttu-id="78977-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="78977-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78977-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78977-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78977-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78977-107">DESCRIPTION</span></span>
<span data-ttu-id="78977-108">Cmdleten **Get-AzDataShareSynchronizationSetting** innehåller information om synkronisering aktive rad på en resurs.</span><span class="sxs-lookup"><span data-stu-id="78977-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="78977-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78977-109">EXAMPLES</span></span>

### <span data-ttu-id="78977-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="78977-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="78977-111">Det här kommandot innehåller information om synkronisering ShareSynchronization aktive rad på Share AdsShare under data Share Account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="78977-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="78977-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78977-112">PARAMETERS</span></span>

### <span data-ttu-id="78977-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78977-113">-AccountName</span></span>
<span data-ttu-id="78977-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="78977-114">Azure data share account name</span></span>

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

### <span data-ttu-id="78977-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78977-115">-DefaultProfile</span></span>
<span data-ttu-id="78977-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78977-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78977-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="78977-117">-Name</span></span>
<span data-ttu-id="78977-118">Namn på synkronisering</span><span class="sxs-lookup"><span data-stu-id="78977-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78977-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78977-119">-ResourceGroupName</span></span>
<span data-ttu-id="78977-120">Resurs grupp namn för Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="78977-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="78977-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78977-121">-ResourceId</span></span>
<span data-ttu-id="78977-122">Resurs-ID för Azure Data Share-synkronisering</span><span class="sxs-lookup"><span data-stu-id="78977-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="78977-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="78977-123">-ShareName</span></span>
<span data-ttu-id="78977-124">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="78977-124">Azure data share name</span></span>

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

### <span data-ttu-id="78977-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78977-125">CommonParameters</span></span>
<span data-ttu-id="78977-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78977-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78977-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78977-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78977-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78977-128">INPUTS</span></span>

### <span data-ttu-id="78977-129">System. String</span><span class="sxs-lookup"><span data-stu-id="78977-129">System.String</span></span>

## <span data-ttu-id="78977-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78977-130">OUTPUTS</span></span>

### <span data-ttu-id="78977-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="78977-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="78977-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78977-132">NOTES</span></span>

## <span data-ttu-id="78977-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78977-133">RELATED LINKS</span></span>
