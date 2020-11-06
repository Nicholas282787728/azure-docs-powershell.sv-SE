---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574184"
---
# <span data-ttu-id="ee106-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee106-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="ee106-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee106-102">SYNOPSIS</span></span>
<span data-ttu-id="ee106-103">Tar bort en autentiseringsuppgift från ett program.</span><span class="sxs-lookup"><span data-stu-id="ee106-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee106-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee106-104">SYNTAX</span></span>

### <span data-ttu-id="ee106-105">ApplicationObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ee106-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee106-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee106-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee106-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee106-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee106-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee106-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee106-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee106-109">DESCRIPTION</span></span>
<span data-ttu-id="ee106-110">Remove-AzureRmADAppCredential cmdleten kan användas för att ta bort en autentiseringsinformation från ett program om det rör sig om ett problem eller när förnyelsen av autentiseringsuppgiften förnyas.</span><span class="sxs-lookup"><span data-stu-id="ee106-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="ee106-111">Programmet identifieras genom att ange objekt-ID: t eller AppId.</span><span class="sxs-lookup"><span data-stu-id="ee106-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="ee106-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="ee106-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="ee106-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee106-113">EXAMPLES</span></span>

### <span data-ttu-id="ee106-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee106-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="ee106-115">Det här kommandot tar bort en autentiseringsinformation från ett program.</span><span class="sxs-lookup"><span data-stu-id="ee106-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="ee106-116">I det här exemplet kommer 9044423a-60a3-45ac-9ab1-09534157ebb att tas bort från programmet.</span><span class="sxs-lookup"><span data-stu-id="ee106-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="ee106-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ee106-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="ee106-118">Det här kommandot tar bort en autentiseringsinformation från ett program.</span><span class="sxs-lookup"><span data-stu-id="ee106-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="ee106-119">I det här exemplet tas alla autentiseringsuppgifter bort från programmet som är associerat med applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="ee106-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="ee106-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee106-120">PARAMETERS</span></span>

### <span data-ttu-id="ee106-121">-Alla</span><span class="sxs-lookup"><span data-stu-id="ee106-121">-All</span></span>
<span data-ttu-id="ee106-122">Växla för att ta bort alla autentiseringsuppgifter som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="ee106-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ee106-123">-ApplicationId</span></span>
<span data-ttu-id="ee106-124">ID för programmet som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="ee106-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee106-125">-DefaultProfile</span></span>
<span data-ttu-id="ee106-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ee106-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee106-127">-Force</span><span class="sxs-lookup"><span data-stu-id="ee106-127">-Force</span></span>
<span data-ttu-id="ee106-128">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ee106-128">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ee106-129">-KeyId</span></span>
<span data-ttu-id="ee106-130">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ee106-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="ee106-131">De viktigaste ID: na för programmet kan erhållas med hjälp av Get-AzureRmADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee106-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ee106-132">-ObjectId</span></span>
<span data-ttu-id="ee106-133">Objekt-ID för programmet som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="ee106-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee106-134">-Confirm</span></span>
<span data-ttu-id="ee106-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee106-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee106-136">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee106-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee106-137">CommonParameters</span></span>
<span data-ttu-id="ee106-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee106-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee106-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee106-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee106-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee106-140">INPUTS</span></span>

### <span data-ttu-id="ee106-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="ee106-141">None</span></span>
<span data-ttu-id="ee106-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ee106-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee106-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee106-143">OUTPUTS</span></span>

## <span data-ttu-id="ee106-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee106-144">NOTES</span></span>

## <span data-ttu-id="ee106-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee106-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee106-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee106-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="ee106-147">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee106-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="ee106-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ee106-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
