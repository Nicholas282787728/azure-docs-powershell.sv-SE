---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0443b9bc3ed2666600f2d119eca5b7173b21e89d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757428"
---
# <span data-ttu-id="62fdd-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="62fdd-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="62fdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="62fdd-103">Skapar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62fdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62fdd-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62fdd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="62fdd-106">Cmdleten **New-AzureRmApiManagementGroup** skapar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="62fdd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="62fdd-108">Exempel 1: skapa en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="62fdd-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="62fdd-109">Det här kommandot skapar en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-109">This command creates a management group.</span></span>

## <span data-ttu-id="62fdd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62fdd-110">PARAMETERS</span></span>

### <span data-ttu-id="62fdd-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="62fdd-111">-Context</span></span>
<span data-ttu-id="62fdd-112">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="62fdd-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fdd-113">-DefaultProfile</span></span>
<span data-ttu-id="62fdd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62fdd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="62fdd-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="62fdd-115">-Description</span></span>
<span data-ttu-id="62fdd-116">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="62fdd-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fdd-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="62fdd-117">-ExternalId</span></span>
<span data-ttu-id="62fdd-118">För externa grupper innehåller den här egenskapen ID för gruppen från den externa identitets leverantören, till exempel. Azure Active Directory-aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; annars är värdet null.</span><span class="sxs-lookup"><span data-stu-id="62fdd-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62fdd-119">-Kund-</span><span class="sxs-lookup"><span data-stu-id="62fdd-119">-GroupId</span></span>
<span data-ttu-id="62fdd-120">Anger ID för den nya hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="62fdd-120">Specifies the identifier of the new management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fdd-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="62fdd-121">-Name</span></span>
<span data-ttu-id="62fdd-122">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="62fdd-122">Specifies the management group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fdd-123">– Skriv</span><span class="sxs-lookup"><span data-stu-id="62fdd-123">-Type</span></span>
<span data-ttu-id="62fdd-124">Grupptyp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-124">Group Type.</span></span> <span data-ttu-id="62fdd-125">Den anpassade gruppen är en användardefinierad grupp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="62fdd-126">System gruppen inkluderar administratör, utvecklare och gäster.</span><span class="sxs-lookup"><span data-stu-id="62fdd-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="62fdd-127">Du kan inte skapa eller uppdatera en system grupp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="62fdd-128">Extern grupp är grupper från extern identitetsprovider som Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="62fdd-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="62fdd-129">Denna parameter är valfri och som standard antas vara en egen grupp.</span><span class="sxs-lookup"><span data-stu-id="62fdd-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: PsApiManagementGroupType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62fdd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fdd-130">CommonParameters</span></span>
<span data-ttu-id="62fdd-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62fdd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fdd-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62fdd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fdd-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62fdd-133">INPUTS</span></span>

### <span data-ttu-id="62fdd-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="62fdd-134">None</span></span>
<span data-ttu-id="62fdd-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="62fdd-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62fdd-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62fdd-136">OUTPUTS</span></span>

### <span data-ttu-id="62fdd-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="62fdd-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="62fdd-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62fdd-138">NOTES</span></span>

## <span data-ttu-id="62fdd-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62fdd-139">RELATED LINKS</span></span>

[<span data-ttu-id="62fdd-140">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="62fdd-140">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="62fdd-141">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="62fdd-141">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="62fdd-142">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="62fdd-142">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


