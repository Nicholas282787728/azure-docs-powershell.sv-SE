---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579860"
---
# <span data-ttu-id="20e73-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20e73-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="20e73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20e73-102">SYNOPSIS</span></span>
<span data-ttu-id="20e73-103">Hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="20e73-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20e73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20e73-104">SYNTAX</span></span>

### <span data-ttu-id="20e73-105">Hämta alla grupper (standard)</span><span class="sxs-lookup"><span data-stu-id="20e73-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20e73-106">Hämta efter grupp-ID</span><span class="sxs-lookup"><span data-stu-id="20e73-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20e73-107">Hitta grupper efter användare</span><span class="sxs-lookup"><span data-stu-id="20e73-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20e73-108">Hitta grupper efter produkt</span><span class="sxs-lookup"><span data-stu-id="20e73-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20e73-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20e73-109">DESCRIPTION</span></span>
<span data-ttu-id="20e73-110">Cmdleten **Get-AzureRmApiManagementGroup** hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="20e73-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="20e73-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20e73-111">EXAMPLES</span></span>

### <span data-ttu-id="20e73-112">Exempel 1: Hämta alla grupper</span><span class="sxs-lookup"><span data-stu-id="20e73-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="20e73-113">Det här kommandot får alla grupper.</span><span class="sxs-lookup"><span data-stu-id="20e73-113">This command gets all groups.</span></span>

### <span data-ttu-id="20e73-114">Exempel 2: Hämta en grupp efter ID</span><span class="sxs-lookup"><span data-stu-id="20e73-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="20e73-115">Det här kommandot får grupp-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="20e73-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="20e73-116">Exempel 3: Hämta en grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="20e73-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="20e73-117">Det här kommandot får gruppen Group0002.</span><span class="sxs-lookup"><span data-stu-id="20e73-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="20e73-118">Exempel 4: Hämta alla användar grupper</span><span class="sxs-lookup"><span data-stu-id="20e73-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="20e73-119">Det här kommandot får alla användar grupper med användar-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="20e73-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="20e73-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20e73-120">PARAMETERS</span></span>

### <span data-ttu-id="20e73-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="20e73-121">-Context</span></span>
<span data-ttu-id="20e73-122">Anger en instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="20e73-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="20e73-123">-Kund-</span><span class="sxs-lookup"><span data-stu-id="20e73-123">-GroupId</span></span>
<span data-ttu-id="20e73-124">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="20e73-124">Specifies the group ID.</span></span>
<span data-ttu-id="20e73-125">Om det anges försöker cmdleten hitta gruppen baserat på identifieraren.</span><span class="sxs-lookup"><span data-stu-id="20e73-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e73-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="20e73-126">-Name</span></span>
<span data-ttu-id="20e73-127">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="20e73-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="20e73-128">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="20e73-128">-ProductId</span></span>
<span data-ttu-id="20e73-129">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="20e73-129">Identifier of existing product.</span></span>
<span data-ttu-id="20e73-130">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="20e73-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="20e73-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="20e73-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e73-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="20e73-132">-UserId</span></span>
<span data-ttu-id="20e73-133">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="20e73-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="20e73-134">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="20e73-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e73-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e73-135">-DefaultProfile</span></span>
<span data-ttu-id="20e73-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20e73-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20e73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e73-137">CommonParameters</span></span>
<span data-ttu-id="20e73-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e73-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e73-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e73-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20e73-140">INPUTS</span></span>

## <span data-ttu-id="20e73-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20e73-141">OUTPUTS</span></span>

### <span data-ttu-id="20e73-142">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="20e73-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="20e73-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20e73-143">NOTES</span></span>

## <span data-ttu-id="20e73-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20e73-144">RELATED LINKS</span></span>

[<span data-ttu-id="20e73-145">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20e73-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="20e73-146">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20e73-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="20e73-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20e73-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


