---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320324"
---
# <span data-ttu-id="4d0c5-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="4d0c5-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="4d0c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0c5-103">Hämtar information om synkroniseringsinformation för en resurs.</span><span class="sxs-lookup"><span data-stu-id="4d0c5-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="4d0c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d0c5-104">SYNTAX</span></span>

### <span data-ttu-id="4d0c5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4d0c5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d0c5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d0c5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d0c5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d0c5-107">DESCRIPTION</span></span>
<span data-ttu-id="4d0c5-108">Cmdleten **Get-AzDataShareSynchronizationDetail** innehåller information om den synkronisering som initierats för en resurs.</span><span class="sxs-lookup"><span data-stu-id="4d0c5-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="4d0c5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d0c5-109">EXAMPLES</span></span>

### <span data-ttu-id="4d0c5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d0c5-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="4d0c5-111">Det här kommandot ger information om synkroniseringsinställningarna för alla data uppsättningar som motsvarar det tillhandahållna synkroniserings-ID: t.</span><span class="sxs-lookup"><span data-stu-id="4d0c5-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="4d0c5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d0c5-112">PARAMETERS</span></span>

### <span data-ttu-id="4d0c5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d0c5-113">-AccountName</span></span>
<span data-ttu-id="4d0c5-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="4d0c5-114">Azure data share account name</span></span>

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

### <span data-ttu-id="4d0c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0c5-115">-DefaultProfile</span></span>
<span data-ttu-id="4d0c5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d0c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d0c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d0c5-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="4d0c5-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4d0c5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d0c5-119">-ResourceId</span></span>
<span data-ttu-id="4d0c5-120">Azure Data Share Resource-ID</span><span class="sxs-lookup"><span data-stu-id="4d0c5-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="4d0c5-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4d0c5-121">-ShareName</span></span>
<span data-ttu-id="4d0c5-122">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="4d0c5-122">Azure data share name</span></span>

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

### <span data-ttu-id="4d0c5-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="4d0c5-123">-SynchronizationId</span></span>
<span data-ttu-id="4d0c5-124">Synkroniserings-ID för delad synkronisering</span><span class="sxs-lookup"><span data-stu-id="4d0c5-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="4d0c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0c5-125">CommonParameters</span></span>
<span data-ttu-id="4d0c5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0c5-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d0c5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0c5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d0c5-128">INPUTS</span></span>

### <span data-ttu-id="4d0c5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4d0c5-129">System.String</span></span>

## <span data-ttu-id="4d0c5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d0c5-130">OUTPUTS</span></span>

### <span data-ttu-id="4d0c5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="4d0c5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="4d0c5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d0c5-132">NOTES</span></span>

## <span data-ttu-id="4d0c5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d0c5-133">RELATED LINKS</span></span>
