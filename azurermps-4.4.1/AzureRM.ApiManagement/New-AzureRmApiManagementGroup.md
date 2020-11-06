---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 8fc237b130e5044e52f47d306d04c42d12fbad81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578632"
---
# <span data-ttu-id="17d12-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="17d12-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="17d12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17d12-102">SYNOPSIS</span></span>
<span data-ttu-id="17d12-103">Skapar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="17d12-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17d12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17d12-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17d12-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17d12-105">DESCRIPTION</span></span>
<span data-ttu-id="17d12-106">Cmdleten **New-AzureRmApiManagementGroup** skapar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="17d12-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="17d12-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17d12-107">EXAMPLES</span></span>

### <span data-ttu-id="17d12-108">Exempel 1: skapa en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="17d12-108">Example 1: Create a management group</span></span>
```
PS C:\>New-AzureRmApiManagementGroup -Context $APImContext -Name "Group0001"
```

<span data-ttu-id="17d12-109">Det här kommandot skapar en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="17d12-109">This command creates a management group.</span></span>

## <span data-ttu-id="17d12-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17d12-110">PARAMETERS</span></span>

### <span data-ttu-id="17d12-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="17d12-111">-Context</span></span>
<span data-ttu-id="17d12-112">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="17d12-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d12-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="17d12-113">-Description</span></span>
<span data-ttu-id="17d12-114">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="17d12-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="17d12-115">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="17d12-115">-ExternalId</span></span>
<span data-ttu-id="17d12-116">För externa grupper innehåller den här egenskapen ID för gruppen från den externa identitets leverantören, till exempel. Azure Active Directory-aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; annars är värdet null.</span><span class="sxs-lookup"><span data-stu-id="17d12-116">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d12-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="17d12-117">-GroupId</span></span>
<span data-ttu-id="17d12-118">Anger ID för den nya hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="17d12-118">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="17d12-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="17d12-119">-Name</span></span>
<span data-ttu-id="17d12-120">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="17d12-120">Specifies the management group name.</span></span>

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

### <span data-ttu-id="17d12-121">– Skriv</span><span class="sxs-lookup"><span data-stu-id="17d12-121">-Type</span></span>
<span data-ttu-id="17d12-122">Grupptyp.</span><span class="sxs-lookup"><span data-stu-id="17d12-122">Group Type.</span></span> <span data-ttu-id="17d12-123">Den anpassade gruppen är en användardefinierad grupp.</span><span class="sxs-lookup"><span data-stu-id="17d12-123">Custom Group is User defined Group.</span></span> <span data-ttu-id="17d12-124">System gruppen inkluderar administratör, utvecklare och gäster.</span><span class="sxs-lookup"><span data-stu-id="17d12-124">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="17d12-125">Du kan inte skapa eller uppdatera en system grupp.</span><span class="sxs-lookup"><span data-stu-id="17d12-125">You cannot create or update a System Group.</span></span>  <span data-ttu-id="17d12-126">Extern grupp är grupper från extern identitetsprovider som Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17d12-126">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="17d12-127">Denna parameter är valfri och som standard antas vara en egen grupp.</span><span class="sxs-lookup"><span data-stu-id="17d12-127">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d12-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d12-128">-DefaultProfile</span></span>
<span data-ttu-id="17d12-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17d12-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17d12-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d12-130">CommonParameters</span></span>
<span data-ttu-id="17d12-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17d12-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d12-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d12-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d12-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17d12-133">INPUTS</span></span>

## <span data-ttu-id="17d12-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17d12-134">OUTPUTS</span></span>

### <span data-ttu-id="17d12-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="17d12-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="17d12-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17d12-136">NOTES</span></span>

## <span data-ttu-id="17d12-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17d12-137">RELATED LINKS</span></span>

[<span data-ttu-id="17d12-138">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="17d12-138">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="17d12-139">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="17d12-139">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="17d12-140">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="17d12-140">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


