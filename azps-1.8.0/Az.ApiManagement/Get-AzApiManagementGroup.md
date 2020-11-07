---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: a8bef03c7ebe7d20e601ece7c25759f590795ef6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743411"
---
# <span data-ttu-id="de843-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="de843-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="de843-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de843-102">SYNOPSIS</span></span>
<span data-ttu-id="de843-103">Hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="de843-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="de843-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de843-104">SYNTAX</span></span>

### <span data-ttu-id="de843-105">GetAllGroups (standard)</span><span class="sxs-lookup"><span data-stu-id="de843-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de843-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="de843-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de843-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="de843-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de843-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="de843-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de843-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de843-109">DESCRIPTION</span></span>
<span data-ttu-id="de843-110">Cmdleten **Get-AzApiManagementGroup** hämtar alla eller specifika API-hanterings grupper.</span><span class="sxs-lookup"><span data-stu-id="de843-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="de843-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de843-111">EXAMPLES</span></span>

### <span data-ttu-id="de843-112">Exempel 1: Hämta alla grupper</span><span class="sxs-lookup"><span data-stu-id="de843-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="de843-113">Det här kommandot får alla grupper.</span><span class="sxs-lookup"><span data-stu-id="de843-113">This command gets all groups.</span></span>

### <span data-ttu-id="de843-114">Exempel 2: Hämta en grupp efter ID</span><span class="sxs-lookup"><span data-stu-id="de843-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="de843-115">Det här kommandot får grupp-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="de843-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="de843-116">Exempel 3: Hämta en grupp efter namn</span><span class="sxs-lookup"><span data-stu-id="de843-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="de843-117">Det här kommandot får gruppen Group0002.</span><span class="sxs-lookup"><span data-stu-id="de843-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="de843-118">Exempel 4: Hämta alla användar grupper</span><span class="sxs-lookup"><span data-stu-id="de843-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="de843-119">Det här kommandot får alla användar grupper med användar-ID: t 0123456789.</span><span class="sxs-lookup"><span data-stu-id="de843-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="de843-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de843-120">PARAMETERS</span></span>

### <span data-ttu-id="de843-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="de843-121">-Context</span></span>
<span data-ttu-id="de843-122">Anger en instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="de843-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="de843-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de843-123">-DefaultProfile</span></span>
<span data-ttu-id="de843-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de843-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de843-125">-Kund-</span><span class="sxs-lookup"><span data-stu-id="de843-125">-GroupId</span></span>
<span data-ttu-id="de843-126">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="de843-126">Specifies the group ID.</span></span>
<span data-ttu-id="de843-127">Om det anges försöker cmdleten hitta gruppen baserat på identifieraren.</span><span class="sxs-lookup"><span data-stu-id="de843-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="de843-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="de843-128">-Name</span></span>
<span data-ttu-id="de843-129">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="de843-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="de843-130">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="de843-130">-ProductId</span></span>
<span data-ttu-id="de843-131">Identifierare för befintlig produkt.</span><span class="sxs-lookup"><span data-stu-id="de843-131">Identifier of existing product.</span></span>
<span data-ttu-id="de843-132">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="de843-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="de843-133">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="de843-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="de843-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="de843-134">-UserId</span></span>
<span data-ttu-id="de843-135">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="de843-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="de843-136">Om det här alternativet anges returneras alla grupper som produkten tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="de843-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="de843-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de843-137">CommonParameters</span></span>
<span data-ttu-id="de843-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de843-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de843-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de843-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de843-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de843-140">INPUTS</span></span>

### <span data-ttu-id="de843-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="de843-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="de843-142">System. String</span><span class="sxs-lookup"><span data-stu-id="de843-142">System.String</span></span>

## <span data-ttu-id="de843-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de843-143">OUTPUTS</span></span>

### <span data-ttu-id="de843-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="de843-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="de843-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de843-145">NOTES</span></span>

## <span data-ttu-id="de843-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de843-146">RELATED LINKS</span></span>

[<span data-ttu-id="de843-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="de843-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="de843-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="de843-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="de843-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="de843-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


