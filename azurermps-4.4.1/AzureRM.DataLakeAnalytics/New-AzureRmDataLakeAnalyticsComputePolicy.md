---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574694"
---
# <span data-ttu-id="49296-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="49296-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="49296-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="49296-102">SYNOPSIS</span></span>
<span data-ttu-id="49296-103">Skapar en princip regel för data Lake Analytics för en specifik AAD-enhet.</span><span class="sxs-lookup"><span data-stu-id="49296-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49296-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="49296-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49296-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="49296-105">DESCRIPTION</span></span>
<span data-ttu-id="49296-106">Den **nya-AzureRmDataLakeAnalyticsComputePolicy** skapar den angivna beräknings princip regeln för en specifik AAD-enhet i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="49296-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="49296-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="49296-107">EXAMPLES</span></span>

### <span data-ttu-id="49296-108">Exempel 1: skapa en beräknings princip med bara en regel</span><span class="sxs-lookup"><span data-stu-id="49296-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="49296-109">Det här kommandot skapar principen "policy" i kontot "contosoadla" för användaren med ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" som säkerställer att de inte kan skicka jobb med mer än 5 parallellitet.</span><span class="sxs-lookup"><span data-stu-id="49296-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="49296-110">Exempel 2: skapa en beräknings princip med båda reglerna</span><span class="sxs-lookup"><span data-stu-id="49296-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="49296-111">Det här kommandot skapar en princip med namnet "policy" i kontot "contosoadla" för användaren med ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" som säkerställer att de inte kan skicka jobb med mer än 5 parallellitet eller med högre prioritet än 100</span><span class="sxs-lookup"><span data-stu-id="49296-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="49296-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="49296-112">PARAMETERS</span></span>

### <span data-ttu-id="49296-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="49296-113">-Account</span></span>
<span data-ttu-id="49296-114">Namnet på kontot som principen ska läggas till för.</span><span class="sxs-lookup"><span data-stu-id="49296-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="49296-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="49296-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="49296-116">Den högsta graden av parallellitet per jobb för den här policyn.</span><span class="sxs-lookup"><span data-stu-id="49296-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="49296-117">Antingen den här, MinPriorityPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="49296-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49296-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="49296-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="49296-119">Den högsta prioritet som stöds per jobb för den här principen.</span><span class="sxs-lookup"><span data-stu-id="49296-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="49296-120">Antingen den här, MaxDegreeOfParallelismPerJob eller båda parametrarna måste anges.</span><span class="sxs-lookup"><span data-stu-id="49296-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49296-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="49296-121">-Name</span></span>
<span data-ttu-id="49296-122">Namnet på den beräknings princip som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="49296-122">Name of the compute policy to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49296-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="49296-123">-ObjectId</span></span>
<span data-ttu-id="49296-124">Azure Active Directory-objekt-ID: t för den användare eller grupp som principen ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="49296-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49296-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="49296-125">-ObjectType</span></span>
<span data-ttu-id="49296-126">Objekt typen Azure Active Directory för det objekt-ID som skickades.</span><span class="sxs-lookup"><span data-stu-id="49296-126">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49296-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49296-127">-ResourceGroupName</span></span>
<span data-ttu-id="49296-128">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="49296-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="49296-129">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="49296-129">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49296-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="49296-130">-Confirm</span></span>
<span data-ttu-id="49296-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="49296-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49296-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49296-132">-WhatIf</span></span>
<span data-ttu-id="49296-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="49296-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49296-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="49296-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49296-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49296-135">-DefaultProfile</span></span>
<span data-ttu-id="49296-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="49296-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49296-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49296-137">CommonParameters</span></span>
<span data-ttu-id="49296-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49296-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49296-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49296-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49296-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="49296-140">INPUTS</span></span>

### <span data-ttu-id="49296-141">System. String</span><span class="sxs-lookup"><span data-stu-id="49296-141">System.String</span></span>
<span data-ttu-id="49296-142">System. GUID system. Int32</span><span class="sxs-lookup"><span data-stu-id="49296-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="49296-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="49296-143">OUTPUTS</span></span>

### <span data-ttu-id="49296-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="49296-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="49296-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="49296-145">NOTES</span></span>

## <span data-ttu-id="49296-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="49296-146">RELATED LINKS</span></span>

