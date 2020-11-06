---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584543"
---
# <span data-ttu-id="65661-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65661-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="65661-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65661-102">SYNOPSIS</span></span>
<span data-ttu-id="65661-103">Filtrerar Active Directory-tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="65661-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65661-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65661-104">SYNTAX</span></span>

### <span data-ttu-id="65661-105">EmptyParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="65661-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65661-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="65661-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65661-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65661-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65661-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="65661-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65661-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65661-109">DESCRIPTION</span></span>
<span data-ttu-id="65661-110">Filtrerar Active Directory-tjänstens huvud objekt.</span><span class="sxs-lookup"><span data-stu-id="65661-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="65661-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65661-111">EXAMPLES</span></span>

### <span data-ttu-id="65661-112">--------------------------Filtrerar tjänstens huvud namn via SPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="65661-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="65661-113">Hämtar tjänstens huvud namn med 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span><span class="sxs-lookup"><span data-stu-id="65661-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="65661-114">--------------------------Filtrerar tjänstens huvud objekt med Sök sträng--------------------------</span><span class="sxs-lookup"><span data-stu-id="65661-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="65661-115">Filtrerar alla AD service-huvudobjekt med namn som börjar med "webben".</span><span class="sxs-lookup"><span data-stu-id="65661-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="65661-116">--------------------------Lista med AD-huvudtjänstens huvud namn--------------------------</span><span class="sxs-lookup"><span data-stu-id="65661-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="65661-117">Hämtar alla AD-tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="65661-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="65661-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65661-118">PARAMETERS</span></span>

### <span data-ttu-id="65661-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="65661-119">-ObjectId</span></span>
<span data-ttu-id="65661-120">Objekt-ID för tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="65661-120">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65661-121">-SearchString</span><span class="sxs-lookup"><span data-stu-id="65661-121">-SearchString</span></span>
<span data-ttu-id="65661-122">Hämtar alla tjänst säkerhets objekt som har visnings namnet inleds med det här värdet.</span><span class="sxs-lookup"><span data-stu-id="65661-122">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65661-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="65661-123">-ServicePrincipalName</span></span>
<span data-ttu-id="65661-124">Tjänstens SPN.</span><span class="sxs-lookup"><span data-stu-id="65661-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65661-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65661-125">-DefaultProfile</span></span>
<span data-ttu-id="65661-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65661-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65661-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65661-127">CommonParameters</span></span>
<span data-ttu-id="65661-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65661-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65661-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65661-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65661-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65661-130">INPUTS</span></span>

## <span data-ttu-id="65661-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65661-131">OUTPUTS</span></span>

### <span data-ttu-id="65661-132">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="65661-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="65661-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65661-133">NOTES</span></span>

## <span data-ttu-id="65661-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65661-134">RELATED LINKS</span></span>

[<span data-ttu-id="65661-135">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65661-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="65661-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65661-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="65661-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="65661-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="65661-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="65661-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="65661-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="65661-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

