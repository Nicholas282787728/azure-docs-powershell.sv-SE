---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321943"
---
# <span data-ttu-id="5f0f5-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f0f5-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="5f0f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0f5-103">Hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="5f0f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f0f5-104">SYNTAX</span></span>

### <span data-ttu-id="5f0f5-105">GetAllGroups (standard)</span><span class="sxs-lookup"><span data-stu-id="5f0f5-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0f5-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="5f0f5-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0f5-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="5f0f5-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0f5-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="5f0f5-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f0f5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f0f5-109">DESCRIPTION</span></span>
<span data-ttu-id="5f0f5-110">Cmdleten **Get-AzApiManagementGroup** hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="5f0f5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f0f5-111">EXAMPLES</span></span>

### <span data-ttu-id="5f0f5-112">Exempel 1: Hämta alla grupper</span><span class="sxs-lookup"><span data-stu-id="5f0f5-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="5f0f5-113">Det här kommandot får alla grupper.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-113">This command gets all groups.</span></span>

### <span data-ttu-id="5f0f5-114">Exempel 2: Hämta en grupp efter ID</span><span class="sxs-lookup"><span data-stu-id="5f0f5-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="5f0f5-115">Det här kommandot får grupp-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="5f0f5-116">Exempel 3: Hämta en grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="5f0f5-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="5f0f5-117">Det här kommandot får gruppen Group0002.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="5f0f5-118">Exempel 4: Hämta alla användar grupper</span><span class="sxs-lookup"><span data-stu-id="5f0f5-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="5f0f5-119">Det här kommandot får alla användar grupper med användar-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="5f0f5-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f0f5-120">PARAMETERS</span></span>

### <span data-ttu-id="5f0f5-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5f0f5-121">-Context</span></span>
<span data-ttu-id="5f0f5-122">Anger en instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="5f0f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0f5-123">-DefaultProfile</span></span>
<span data-ttu-id="5f0f5-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f0f5-125">-Kund-</span><span class="sxs-lookup"><span data-stu-id="5f0f5-125">-GroupId</span></span>
<span data-ttu-id="5f0f5-126">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-126">Specifies the group ID.</span></span>
<span data-ttu-id="5f0f5-127">Om det anges försöker cmdleten hitta gruppen baserat på identifieraren.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="5f0f5-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f0f5-128">-Name</span></span>
<span data-ttu-id="5f0f5-129">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="5f0f5-130">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="5f0f5-130">-ProductId</span></span>
<span data-ttu-id="5f0f5-131">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-131">Identifier of existing product.</span></span>
<span data-ttu-id="5f0f5-132">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="5f0f5-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f0f5-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="5f0f5-134">-UserId</span></span>
<span data-ttu-id="5f0f5-135">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="5f0f5-136">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="5f0f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0f5-137">CommonParameters</span></span>
<span data-ttu-id="5f0f5-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f0f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0f5-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f0f5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0f5-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f0f5-140">INPUTS</span></span>

### <span data-ttu-id="5f0f5-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f0f5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5f0f5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5f0f5-142">System.String</span></span>

## <span data-ttu-id="5f0f5-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f0f5-143">OUTPUTS</span></span>

### <span data-ttu-id="5f0f5-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f0f5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="5f0f5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f0f5-145">NOTES</span></span>

## <span data-ttu-id="5f0f5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f0f5-146">RELATED LINKS</span></span>

[<span data-ttu-id="5f0f5-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f0f5-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="5f0f5-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f0f5-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="5f0f5-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5f0f5-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


