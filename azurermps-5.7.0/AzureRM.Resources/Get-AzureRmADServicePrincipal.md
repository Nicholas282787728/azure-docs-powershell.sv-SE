---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575538"
---
# <span data-ttu-id="63166-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63166-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="63166-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63166-102">SYNOPSIS</span></span>
<span data-ttu-id="63166-103">Filtrerar Active Directory-tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="63166-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63166-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63166-104">SYNTAX</span></span>

### <span data-ttu-id="63166-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="63166-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63166-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="63166-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63166-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63166-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63166-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="63166-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63166-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63166-109">DESCRIPTION</span></span>
<span data-ttu-id="63166-110">Filtrerar Active Directory-tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="63166-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="63166-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63166-111">EXAMPLES</span></span>

### <span data-ttu-id="63166-112">Filtrerar tjänstens huvud objekt med SPN</span><span class="sxs-lookup"><span data-stu-id="63166-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="63166-113">Hämtar tjänstens huvud namn med 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span><span class="sxs-lookup"><span data-stu-id="63166-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="63166-114">Filtrerar tjänstens huvud objekt med Sök sträng</span><span class="sxs-lookup"><span data-stu-id="63166-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="63166-115">Filtrerar alla AD service-huvudobjekt med namn som börjar med "webben".</span><span class="sxs-lookup"><span data-stu-id="63166-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="63166-116">Visa AD-huvudtjänstens huvud namn</span><span class="sxs-lookup"><span data-stu-id="63166-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="63166-117">Hämtar alla AD-tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="63166-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="63166-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63166-118">PARAMETERS</span></span>

### <span data-ttu-id="63166-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63166-119">-DefaultProfile</span></span>
<span data-ttu-id="63166-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="63166-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63166-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="63166-121">-ObjectId</span></span>
<span data-ttu-id="63166-122">Objekt-ID för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="63166-122">Object id of the service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63166-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="63166-123">-SearchString</span></span>
<span data-ttu-id="63166-124">Hämtar alla tjänst säkerhets objekt som har visnings namnet inleds med det här värdet.</span><span class="sxs-lookup"><span data-stu-id="63166-124">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63166-125">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="63166-125">-ServicePrincipalName</span></span>
<span data-ttu-id="63166-126">Tjänstens SPN.</span><span class="sxs-lookup"><span data-stu-id="63166-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63166-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63166-127">CommonParameters</span></span>
<span data-ttu-id="63166-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63166-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63166-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63166-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63166-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63166-130">INPUTS</span></span>

### <span data-ttu-id="63166-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="63166-131">None</span></span>
<span data-ttu-id="63166-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="63166-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63166-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63166-133">OUTPUTS</span></span>

### <span data-ttu-id="63166-134">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="63166-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="63166-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63166-135">NOTES</span></span>

## <span data-ttu-id="63166-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63166-136">RELATED LINKS</span></span>

[<span data-ttu-id="63166-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63166-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="63166-138">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63166-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="63166-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63166-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="63166-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="63166-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="63166-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="63166-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

