---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525099"
---
# <span data-ttu-id="5eab1-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="5eab1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5eab1-102">SYNOPSIS</span></span>
<span data-ttu-id="5eab1-103">Hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="5eab1-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="5eab1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5eab1-104">SYNTAX</span></span>

### <span data-ttu-id="5eab1-105">GetAllGroups (standard)</span><span class="sxs-lookup"><span data-stu-id="5eab1-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eab1-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="5eab1-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eab1-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="5eab1-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eab1-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5eab1-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eab1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5eab1-109">DESCRIPTION</span></span>
<span data-ttu-id="5eab1-110">Cmdleten **Get-AzApiManagementGroup** hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="5eab1-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="5eab1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5eab1-111">EXAMPLES</span></span>

### <span data-ttu-id="5eab1-112">Exempel 1: Hämta alla grupper</span><span class="sxs-lookup"><span data-stu-id="5eab1-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="5eab1-113">Det här kommandot får alla grupper.</span><span class="sxs-lookup"><span data-stu-id="5eab1-113">This command gets all groups.</span></span>

### <span data-ttu-id="5eab1-114">Exempel 2: Hämta en grupp efter ID</span><span class="sxs-lookup"><span data-stu-id="5eab1-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="5eab1-115">Det här kommandot får grupp-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5eab1-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="5eab1-116">Exempel 3: Hämta en grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="5eab1-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="5eab1-117">Det här kommandot får gruppen Group0002.</span><span class="sxs-lookup"><span data-stu-id="5eab1-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="5eab1-118">Exempel 4: Hämta alla användar grupper</span><span class="sxs-lookup"><span data-stu-id="5eab1-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5eab1-119">Det här kommandot får alla användar grupper med användar-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5eab1-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="5eab1-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5eab1-120">PARAMETERS</span></span>

### <span data-ttu-id="5eab1-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5eab1-121">-Context</span></span>
<span data-ttu-id="5eab1-122">Anger en instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5eab1-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eab1-123">-DefaultProfile</span></span>
<span data-ttu-id="5eab1-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5eab1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eab1-125">-Kund-</span><span class="sxs-lookup"><span data-stu-id="5eab1-125">-GroupId</span></span>
<span data-ttu-id="5eab1-126">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="5eab1-126">Specifies the group ID.</span></span>
<span data-ttu-id="5eab1-127">Om det anges försöker cmdleten hitta gruppen baserat på identifieraren.</span><span class="sxs-lookup"><span data-stu-id="5eab1-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="5eab1-128">-Name</span></span>
<span data-ttu-id="5eab1-129">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="5eab1-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="5eab1-130">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="5eab1-130">-ProductId</span></span>
<span data-ttu-id="5eab1-131">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="5eab1-131">Identifier of existing product.</span></span>
<span data-ttu-id="5eab1-132">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="5eab1-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="5eab1-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="5eab1-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="5eab1-134">-UserId</span></span>
<span data-ttu-id="5eab1-135">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="5eab1-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="5eab1-136">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="5eab1-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eab1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eab1-137">CommonParameters</span></span>
<span data-ttu-id="5eab1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eab1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eab1-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eab1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eab1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5eab1-140">INPUTS</span></span>

### <span data-ttu-id="5eab1-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5eab1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5eab1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5eab1-142">System.String</span></span>

## <span data-ttu-id="5eab1-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5eab1-143">OUTPUTS</span></span>

### <span data-ttu-id="5eab1-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="5eab1-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5eab1-145">NOTES</span></span>

## <span data-ttu-id="5eab1-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5eab1-146">RELATED LINKS</span></span>

[<span data-ttu-id="5eab1-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="5eab1-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="5eab1-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5eab1-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


