---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581300"
---
# <span data-ttu-id="4ee03-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4ee03-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="4ee03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ee03-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee03-103">Tar bort en autentiseringsuppgift från ett program.</span><span class="sxs-lookup"><span data-stu-id="4ee03-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ee03-104">SYNTAX</span></span>

### <span data-ttu-id="4ee03-105">ApplicationObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4ee03-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee03-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee03-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee03-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee03-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee03-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee03-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee03-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ee03-109">DESCRIPTION</span></span>
<span data-ttu-id="4ee03-110">Remove-AzureRmADAppCredential cmdleten kan användas för att ta bort en autentiseringsinformation från ett program om det rör sig om ett problem eller när förnyelsen av autentiseringsuppgiften förnyas.</span><span class="sxs-lookup"><span data-stu-id="4ee03-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="4ee03-111">Programmet identifieras genom att ange objekt-ID: t eller AppId.</span><span class="sxs-lookup"><span data-stu-id="4ee03-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="4ee03-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="4ee03-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="4ee03-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ee03-113">EXAMPLES</span></span>

### <span data-ttu-id="4ee03-114">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ee03-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="4ee03-115">Det här kommandot tar bort en autentiseringsinformation från ett program.</span><span class="sxs-lookup"><span data-stu-id="4ee03-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="4ee03-116">I det här exemplet kommer 9044423a-60a3-45ac-9ab1-09534157ebb att tas bort från programmet.</span><span class="sxs-lookup"><span data-stu-id="4ee03-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="4ee03-117">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ee03-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="4ee03-118">Det här kommandot tar bort en autentiseringsinformation från ett program.</span><span class="sxs-lookup"><span data-stu-id="4ee03-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="4ee03-119">I det här exemplet tas alla autentiseringsuppgifter bort från programmet som är associerat med applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="4ee03-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="4ee03-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ee03-120">PARAMETERS</span></span>

### <span data-ttu-id="4ee03-121">-Alla</span><span class="sxs-lookup"><span data-stu-id="4ee03-121">-All</span></span>
<span data-ttu-id="4ee03-122">Växla för att ta bort alla autentiseringsuppgifter som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="4ee03-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee03-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4ee03-123">-ApplicationId</span></span>
<span data-ttu-id="4ee03-124">ID för programmet som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="4ee03-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee03-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4ee03-125">-Force</span></span>
<span data-ttu-id="4ee03-126">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4ee03-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee03-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="4ee03-127">-KeyId</span></span>
<span data-ttu-id="4ee03-128">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4ee03-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="4ee03-129">De viktigaste ID: na för programmet kan erhållas med hjälp av Get-AzureRmADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee03-129">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee03-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4ee03-130">-ObjectId</span></span>
<span data-ttu-id="4ee03-131">Objekt-ID för programmet som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="4ee03-131">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee03-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ee03-132">-Confirm</span></span>
<span data-ttu-id="4ee03-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ee03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee03-134">-WhatIf</span></span>
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

### <span data-ttu-id="4ee03-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee03-135">-DefaultProfile</span></span>
<span data-ttu-id="4ee03-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee03-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee03-137">CommonParameters</span></span>
<span data-ttu-id="4ee03-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee03-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee03-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee03-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ee03-140">INPUTS</span></span>

## <span data-ttu-id="4ee03-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ee03-141">OUTPUTS</span></span>

## <span data-ttu-id="4ee03-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ee03-142">NOTES</span></span>

## <span data-ttu-id="4ee03-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ee03-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ee03-144">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4ee03-144">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="4ee03-145">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4ee03-145">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="4ee03-146">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4ee03-146">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
