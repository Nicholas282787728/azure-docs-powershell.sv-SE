---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576800"
---
# <span data-ttu-id="9de6d-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9de6d-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="9de6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9de6d-102">SYNOPSIS</span></span>
<span data-ttu-id="9de6d-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="9de6d-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9de6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9de6d-104">SYNTAX</span></span>

### <span data-ttu-id="9de6d-105">ApplicationObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9de6d-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de6d-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de6d-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9de6d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de6d-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9de6d-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de6d-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9de6d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9de6d-109">DESCRIPTION</span></span>
<span data-ttu-id="9de6d-110">Med cmdleten Get-AzureRmADAppCredential kan du hämta en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="9de6d-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="9de6d-111">Det här kommandot hämtar alla autentiseringsuppgifter-egenskaper (men inte referensvärdet) som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="9de6d-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="9de6d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9de6d-112">EXAMPLES</span></span>

### <span data-ttu-id="9de6d-113">Exempel 1 – få programautentisering genom objekt-ID</span><span class="sxs-lookup"><span data-stu-id="9de6d-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="9de6d-114">Returnerar en lista med autentiseringsuppgifter som är kopplade till programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="9de6d-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="9de6d-115">Exempel 2 – få programautentiseringsuppgifter genom rör</span><span class="sxs-lookup"><span data-stu-id="9de6d-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="9de6d-116">Hämtar programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' och kopplas till Get-AzureRmADAppCredential cmdlet för att lista alla autentiseringsuppgifter för det programmet.</span><span class="sxs-lookup"><span data-stu-id="9de6d-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="9de6d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9de6d-117">PARAMETERS</span></span>

### <span data-ttu-id="9de6d-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9de6d-118">-ApplicationId</span></span>
<span data-ttu-id="9de6d-119">ID för programmet som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="9de6d-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de6d-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9de6d-120">-ApplicationObject</span></span>
<span data-ttu-id="9de6d-121">Application-objektet som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="9de6d-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9de6d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de6d-122">-DefaultProfile</span></span>
<span data-ttu-id="9de6d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9de6d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9de6d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9de6d-124">-DisplayName</span></span>
<span data-ttu-id="9de6d-125">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="9de6d-125">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de6d-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9de6d-126">-ObjectId</span></span>
<span data-ttu-id="9de6d-127">Objekt-ID för programmet som du vill hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="9de6d-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de6d-128">CommonParameters</span></span>
<span data-ttu-id="9de6d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de6d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de6d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de6d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9de6d-131">INPUTS</span></span>

### <span data-ttu-id="9de6d-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9de6d-132">System.Guid</span></span>

### <span data-ttu-id="9de6d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9de6d-133">System.String</span></span>

### <span data-ttu-id="9de6d-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9de6d-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="9de6d-135">Parametrar: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9de6d-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="9de6d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9de6d-136">OUTPUTS</span></span>

### <span data-ttu-id="9de6d-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9de6d-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9de6d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9de6d-138">NOTES</span></span>

## <span data-ttu-id="9de6d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9de6d-139">RELATED LINKS</span></span>

[<span data-ttu-id="9de6d-140">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9de6d-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="9de6d-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9de6d-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="9de6d-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="9de6d-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

