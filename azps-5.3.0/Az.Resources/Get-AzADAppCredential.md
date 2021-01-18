---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521620"
---
# <span data-ttu-id="14216-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="14216-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="14216-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14216-102">SYNOPSIS</span></span>
<span data-ttu-id="14216-103">Hämtar en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="14216-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="14216-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14216-104">SYNTAX</span></span>

### <span data-ttu-id="14216-105">ApplicationObjectIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="14216-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14216-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14216-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14216-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14216-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14216-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14216-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14216-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14216-109">DESCRIPTION</span></span>
<span data-ttu-id="14216-110">Med cmdleten Get-AzADAppCredential kan du hämta en lista med autentiseringsuppgifter som är associerade med ett program.</span><span class="sxs-lookup"><span data-stu-id="14216-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="14216-111">Det här kommandot hämtar alla autentiseringsuppgifter-egenskaper (men inte referensvärdet) som är associerade med programmet.</span><span class="sxs-lookup"><span data-stu-id="14216-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="14216-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14216-112">EXAMPLES</span></span>

### <span data-ttu-id="14216-113">Exempel 1: Hämta programautentiseringsuppgifter genom objekt-ID</span><span class="sxs-lookup"><span data-stu-id="14216-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="14216-114">Returnerar en lista med autentiseringsuppgifter som är kopplade till programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="14216-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="14216-115">Exempel 2: Hämta programautentiseringsuppgifter genom rör</span><span class="sxs-lookup"><span data-stu-id="14216-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="14216-116">Hämtar programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' och kopplas till Get-AzADAppCredential cmdlet för att lista alla autentiseringsuppgifter för det programmet.</span><span class="sxs-lookup"><span data-stu-id="14216-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="14216-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14216-117">PARAMETERS</span></span>

### <span data-ttu-id="14216-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="14216-118">-ApplicationId</span></span>
<span data-ttu-id="14216-119">ID för programmet som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="14216-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="14216-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="14216-120">-ApplicationObject</span></span>
<span data-ttu-id="14216-121">Application-objektet som autentiseringsuppgifterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="14216-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14216-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14216-122">-DefaultProfile</span></span>
<span data-ttu-id="14216-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="14216-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14216-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14216-124">-DisplayName</span></span>
<span data-ttu-id="14216-125">Programmets visnings namn.</span><span class="sxs-lookup"><span data-stu-id="14216-125">The display name of the application.</span></span>

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

### <span data-ttu-id="14216-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="14216-126">-ObjectId</span></span>
<span data-ttu-id="14216-127">Objekt-ID för programmet som du vill hämta autentiseringsuppgifter från.</span><span class="sxs-lookup"><span data-stu-id="14216-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14216-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14216-128">CommonParameters</span></span>
<span data-ttu-id="14216-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14216-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14216-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14216-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14216-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14216-131">INPUTS</span></span>

### <span data-ttu-id="14216-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14216-132">System.String</span></span>

### <span data-ttu-id="14216-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="14216-133">System.Guid</span></span>

### <span data-ttu-id="14216-134">Microsoft. Azure. commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="14216-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="14216-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14216-135">OUTPUTS</span></span>

### <span data-ttu-id="14216-136">Microsoft. Azure. commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="14216-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="14216-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14216-137">NOTES</span></span>

## <span data-ttu-id="14216-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14216-138">RELATED LINKS</span></span>

[<span data-ttu-id="14216-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="14216-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="14216-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="14216-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="14216-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="14216-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

