---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 67af78e767b8da7764053e3652e25aef53f2877e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581280"
---
# <span data-ttu-id="e247a-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e247a-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="e247a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e247a-102">SYNOPSIS</span></span>
<span data-ttu-id="e247a-103">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e247a-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e247a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e247a-104">SYNTAX</span></span>

### <span data-ttu-id="e247a-105">SpObjectIdWithDisplayNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e247a-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e247a-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e247a-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e247a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e247a-107">DESCRIPTION</span></span>
<span data-ttu-id="e247a-108">Uppdaterar ett befintligt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e247a-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="e247a-109">Använd New-AzureRmADSpCredential cmdlet för att uppdatera autentiseringsuppgifterna som är associerade med den här tjänstens huvud säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="e247a-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="e247a-110">Använd Set-AzureRmADApplication cmdlet för att uppdatera egenskaperna för det underliggande programmet.</span><span class="sxs-lookup"><span data-stu-id="e247a-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="e247a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e247a-111">EXAMPLES</span></span>

### <span data-ttu-id="e247a-112">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e247a-112">--------------------------  Example 1  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="e247a-113">Uppdaterar visnings namnet för tjänstens huvud konto med angivet objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="e247a-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="e247a-114">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e247a-114">--------------------------  Example 2  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="e247a-115">Uppdaterar visnings namnet för tjänstens huvud namn med angivet SPN.</span><span class="sxs-lookup"><span data-stu-id="e247a-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="e247a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e247a-116">PARAMETERS</span></span>

### <span data-ttu-id="e247a-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e247a-117">-DisplayName</span></span>
<span data-ttu-id="e247a-118">Nytt visnings namn för tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="e247a-118">New display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247a-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e247a-119">-ObjectId</span></span>
<span data-ttu-id="e247a-120">Objekt-ID för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="e247a-120">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247a-121">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e247a-121">-ServicePrincipalName</span></span>
<span data-ttu-id="e247a-122">SPN för tjänstens huvud namn att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="e247a-122">The SPN of service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e247a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e247a-123">-Confirm</span></span>
<span data-ttu-id="e247a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e247a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e247a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e247a-125">-WhatIf</span></span>
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

### <span data-ttu-id="e247a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e247a-126">-DefaultProfile</span></span>
<span data-ttu-id="e247a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e247a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e247a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e247a-128">CommonParameters</span></span>
<span data-ttu-id="e247a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e247a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e247a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e247a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e247a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e247a-131">INPUTS</span></span>

## <span data-ttu-id="e247a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e247a-132">OUTPUTS</span></span>

## <span data-ttu-id="e247a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e247a-133">NOTES</span></span>

## <span data-ttu-id="e247a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e247a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e247a-135">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e247a-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e247a-136">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e247a-136">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e247a-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e247a-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e247a-138">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e247a-138">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="e247a-139">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e247a-139">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="e247a-140">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e247a-140">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

