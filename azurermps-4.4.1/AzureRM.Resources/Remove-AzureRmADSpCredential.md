---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757477"
---
# <span data-ttu-id="83c65-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="83c65-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="83c65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83c65-102">SYNOPSIS</span></span>
<span data-ttu-id="83c65-103">Tar bort en autentiseringsuppgift från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="83c65-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83c65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83c65-104">SYNTAX</span></span>

### <span data-ttu-id="83c65-105">ObjectIdWithKeyIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="83c65-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c65-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="83c65-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c65-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83c65-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c65-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="83c65-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83c65-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83c65-109">DESCRIPTION</span></span>
<span data-ttu-id="83c65-110">Du kan använda Remove-AzureRmADSpCredential cmdlet för att ta bort en behörighets nycklar från ett säkerhets objekt om det rör sig om en kompromiss eller en del av förnyelsen av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="83c65-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="83c65-111">Tjänstens huvud namn identifieras genom att ange antingen objekt-ID eller SPN (Service Principal Name).</span><span class="sxs-lookup"><span data-stu-id="83c65-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="83c65-112">Den autentiseringsuppgift som ska tas bort identifieras via dess tillhör ande ID om en enskild autentiseringsuppgift ska tas bort eller med en "alla"-växel för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="83c65-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="83c65-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83c65-113">EXAMPLES</span></span>

### <span data-ttu-id="83c65-114">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83c65-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="83c65-115">Det här kommandot tar bort en autentiseringsinformation från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="83c65-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="83c65-116">I det här exemplet kommer 9044423a-60a3-45ac-9ab1-09534157ebb att tas bort från tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="83c65-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="83c65-117">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="83c65-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="83c65-118">Det här kommandot tar bort en autentiseringsinformation från ett tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="83c65-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="83c65-119">I det här exemplet kommer alla autentiseringsuppgifter att tas bort från tjänstens huvud namn som är kopplat till tjänst huvud namnet " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="83c65-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="83c65-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83c65-120">PARAMETERS</span></span>

### <span data-ttu-id="83c65-121">-Alla</span><span class="sxs-lookup"><span data-stu-id="83c65-121">-All</span></span>
<span data-ttu-id="83c65-122">Växla för att ta bort alla autentiseringsuppgifter som är kopplade till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="83c65-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c65-123">-Force</span><span class="sxs-lookup"><span data-stu-id="83c65-123">-Force</span></span>
<span data-ttu-id="83c65-124">Växla till att ta bort autentiseringsuppgiften utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="83c65-124">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="83c65-125">-KeyId</span><span class="sxs-lookup"><span data-stu-id="83c65-125">-KeyId</span></span>
<span data-ttu-id="83c65-126">Anger den autentiseringsinformation som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="83c65-126">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="83c65-127">Huvud-ID: na för ett tjänst huvud konto kan erhållas med hjälp av Get-AzureRmADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83c65-127">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c65-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="83c65-128">-ObjectId</span></span>
<span data-ttu-id="83c65-129">Objekt-ID för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="83c65-129">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c65-130">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="83c65-130">-ServicePrincipalName</span></span>
<span data-ttu-id="83c65-131">Namnet (SPN) för tjänstens huvud namn som autentiseringsuppgifterna ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="83c65-131">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c65-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83c65-132">-Confirm</span></span>
<span data-ttu-id="83c65-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83c65-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83c65-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83c65-134">-WhatIf</span></span>
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

### <span data-ttu-id="83c65-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c65-135">-DefaultProfile</span></span>
<span data-ttu-id="83c65-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83c65-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83c65-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c65-137">CommonParameters</span></span>
<span data-ttu-id="83c65-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c65-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c65-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83c65-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c65-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83c65-140">INPUTS</span></span>

## <span data-ttu-id="83c65-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83c65-141">OUTPUTS</span></span>

## <span data-ttu-id="83c65-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83c65-142">NOTES</span></span>

## <span data-ttu-id="83c65-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83c65-143">RELATED LINKS</span></span>

[<span data-ttu-id="83c65-144">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="83c65-144">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="83c65-145">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="83c65-145">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="83c65-146">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="83c65-146">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

