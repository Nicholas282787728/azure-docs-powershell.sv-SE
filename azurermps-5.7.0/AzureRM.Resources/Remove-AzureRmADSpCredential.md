---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583064"
---
# <span data-ttu-id="2afe2-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2afe2-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="2afe2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2afe2-102">SYNOPSIS</span></span>
<span data-ttu-id="2afe2-103">Tar bort en autentiseringsuppgift från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="2afe2-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2afe2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2afe2-104">SYNTAX</span></span>

### <span data-ttu-id="2afe2-105">ObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2afe2-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe2-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="2afe2-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe2-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2afe2-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afe2-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="2afe2-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2afe2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2afe2-109">DESCRIPTION</span></span>
<span data-ttu-id="2afe2-110">Du kan använda Remove-AzureRmADSpCredential cmdlet för att ta bort en behörighets nycklar från ett säkerhets objekt om det rör sig om en kompromiss eller en del av förnyelsen av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="2afe2-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="2afe2-111">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID eller SPN (Service Principal Name).</span><span class="sxs-lookup"><span data-stu-id="2afe2-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="2afe2-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="2afe2-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="2afe2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2afe2-113">EXAMPLES</span></span>

### <span data-ttu-id="2afe2-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2afe2-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="2afe2-115">Det här kommandot tar bort en autentiseringsinformation från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="2afe2-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="2afe2-116">I det här exemplet kommer 9044423a-60a3-45ac-9ab1-09534157ebb att tas bort från tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="2afe2-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="2afe2-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2afe2-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="2afe2-118">Det här kommandot tar bort en autentiseringsinformation från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="2afe2-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="2afe2-119">I det här exemplet kommer alla autentiseringsuppgifter att tas bort från tjänstens huvud namn som är kopplat till tjänst huvud namnet " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="2afe2-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="2afe2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2afe2-120">PARAMETERS</span></span>

### <span data-ttu-id="2afe2-121">-Alla</span><span class="sxs-lookup"><span data-stu-id="2afe2-121">-All</span></span>
<span data-ttu-id="2afe2-122">Växla för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="2afe2-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afe2-123">-DefaultProfile</span></span>
<span data-ttu-id="2afe2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2afe2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2afe2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2afe2-125">-Force</span></span>
<span data-ttu-id="2afe2-126">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2afe2-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="2afe2-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2afe2-127">-KeyId</span></span>
<span data-ttu-id="2afe2-128">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2afe2-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="2afe2-129">Huvud-ID: na för ett tjänst huvud konto kan erhållas med hjälp av Get-AzureRmADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2afe2-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe2-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2afe2-130">-ObjectId</span></span>
<span data-ttu-id="2afe2-131">Objekt-ID för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="2afe2-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe2-132">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2afe2-132">-ServicePrincipalName</span></span>
<span data-ttu-id="2afe2-133">Namnet (SPN) för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="2afe2-133">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe2-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2afe2-134">-Confirm</span></span>
<span data-ttu-id="2afe2-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2afe2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2afe2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2afe2-136">-WhatIf</span></span>
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

### <span data-ttu-id="2afe2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afe2-137">CommonParameters</span></span>
<span data-ttu-id="2afe2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2afe2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afe2-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afe2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afe2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2afe2-140">INPUTS</span></span>

### <span data-ttu-id="2afe2-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="2afe2-141">None</span></span>
<span data-ttu-id="2afe2-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2afe2-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2afe2-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2afe2-143">OUTPUTS</span></span>

## <span data-ttu-id="2afe2-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2afe2-144">NOTES</span></span>

## <span data-ttu-id="2afe2-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2afe2-145">RELATED LINKS</span></span>

[<span data-ttu-id="2afe2-146">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2afe2-146">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="2afe2-147">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2afe2-147">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="2afe2-148">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2afe2-148">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

