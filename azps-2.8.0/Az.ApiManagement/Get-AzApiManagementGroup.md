---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 9a8acd17f953e90cd5b4311854830da03dc4df0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745839"
---
# <span data-ttu-id="c52eb-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c52eb-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="c52eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c52eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c52eb-103">Hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="c52eb-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="c52eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c52eb-104">SYNTAX</span></span>

### <span data-ttu-id="c52eb-105">GetAllGroups (standard)</span><span class="sxs-lookup"><span data-stu-id="c52eb-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c52eb-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="c52eb-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c52eb-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="c52eb-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c52eb-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="c52eb-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c52eb-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c52eb-109">DESCRIPTION</span></span>
<span data-ttu-id="c52eb-110">Cmdleten **Get-AzApiManagementGroup** hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="c52eb-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="c52eb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c52eb-111">EXAMPLES</span></span>

### <span data-ttu-id="c52eb-112">Exempel 1: Hämta alla grupper</span><span class="sxs-lookup"><span data-stu-id="c52eb-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="c52eb-113">Det här kommandot får alla grupper.</span><span class="sxs-lookup"><span data-stu-id="c52eb-113">This command gets all groups.</span></span>

### <span data-ttu-id="c52eb-114">Exempel 2: Hämta en grupp efter ID</span><span class="sxs-lookup"><span data-stu-id="c52eb-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="c52eb-115">Det här kommandot får grupp-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="c52eb-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="c52eb-116">Exempel 3: Hämta en grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="c52eb-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="c52eb-117">Det här kommandot får gruppen Group0002.</span><span class="sxs-lookup"><span data-stu-id="c52eb-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="c52eb-118">Exempel 4: Hämta alla användar grupper</span><span class="sxs-lookup"><span data-stu-id="c52eb-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="c52eb-119">Det här kommandot får alla användar grupper med användar-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="c52eb-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="c52eb-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c52eb-120">PARAMETERS</span></span>

### <span data-ttu-id="c52eb-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c52eb-121">-Context</span></span>
<span data-ttu-id="c52eb-122">Anger en instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c52eb-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="c52eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52eb-123">-DefaultProfile</span></span>
<span data-ttu-id="c52eb-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c52eb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c52eb-125">-Kund-</span><span class="sxs-lookup"><span data-stu-id="c52eb-125">-GroupId</span></span>
<span data-ttu-id="c52eb-126">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="c52eb-126">Specifies the group ID.</span></span>
<span data-ttu-id="c52eb-127">Om det anges försöker cmdleten hitta gruppen baserat på identifieraren.</span><span class="sxs-lookup"><span data-stu-id="c52eb-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="c52eb-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="c52eb-128">-Name</span></span>
<span data-ttu-id="c52eb-129">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="c52eb-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="c52eb-130">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="c52eb-130">-ProductId</span></span>
<span data-ttu-id="c52eb-131">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="c52eb-131">Identifier of existing product.</span></span>
<span data-ttu-id="c52eb-132">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="c52eb-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="c52eb-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c52eb-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="c52eb-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="c52eb-134">-UserId</span></span>
<span data-ttu-id="c52eb-135">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="c52eb-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="c52eb-136">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="c52eb-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="c52eb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52eb-137">CommonParameters</span></span>
<span data-ttu-id="c52eb-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c52eb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52eb-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c52eb-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52eb-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c52eb-140">INPUTS</span></span>

### <span data-ttu-id="c52eb-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c52eb-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c52eb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c52eb-142">System.String</span></span>

## <span data-ttu-id="c52eb-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c52eb-143">OUTPUTS</span></span>

### <span data-ttu-id="c52eb-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c52eb-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="c52eb-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c52eb-145">NOTES</span></span>

## <span data-ttu-id="c52eb-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c52eb-146">RELATED LINKS</span></span>

[<span data-ttu-id="c52eb-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c52eb-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="c52eb-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c52eb-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="c52eb-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c52eb-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


