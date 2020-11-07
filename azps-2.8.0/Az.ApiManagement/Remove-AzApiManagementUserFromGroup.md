---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 73d21a78fd71a677c03e52e131abb7050d71fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745689"
---
# <span data-ttu-id="7a7d3-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="7a7d3-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="7a7d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7d3-103">Tar bort en användare från en grupp.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-103">Removes a user from a group.</span></span>

## <span data-ttu-id="7a7d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a7d3-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a7d3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7d3-106">Cmdleten **Remove-AzApiManagementUserFromGroup** tar bort en användare från en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="7a7d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a7d3-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7d3-108">Exempel 1: ta bort en användare från en grupp</span><span class="sxs-lookup"><span data-stu-id="7a7d3-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="7a7d3-109">Det här kommandot tar bort en användare från en grupp.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="7a7d3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a7d3-110">PARAMETERS</span></span>

### <span data-ttu-id="7a7d3-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7a7d3-111">-Context</span></span>
<span data-ttu-id="7a7d3-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7a7d3-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7a7d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7d3-114">-DefaultProfile</span></span>
<span data-ttu-id="7a7d3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7d3-116">-Kund-</span><span class="sxs-lookup"><span data-stu-id="7a7d3-116">-GroupId</span></span>
<span data-ttu-id="7a7d3-117">Anger ID för den grupp som du vill ta bort en användare från.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="7a7d3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a7d3-118">-PassThru</span></span>
<span data-ttu-id="7a7d3-119">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7d3-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="7a7d3-120">-UserId</span></span>
<span data-ttu-id="7a7d3-121">Anger ID: t för den användare som ska tas bort från gruppen.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="7a7d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7d3-122">CommonParameters</span></span>
<span data-ttu-id="7a7d3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7d3-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a7d3-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7d3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a7d3-125">INPUTS</span></span>

### <span data-ttu-id="7a7d3-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7a7d3-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a7d3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7d3-127">System.String</span></span>

### <span data-ttu-id="7a7d3-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a7d3-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a7d3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a7d3-129">OUTPUTS</span></span>

### <span data-ttu-id="7a7d3-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a7d3-130">System.Boolean</span></span>

## <span data-ttu-id="7a7d3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a7d3-131">NOTES</span></span>

## <span data-ttu-id="7a7d3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a7d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="7a7d3-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="7a7d3-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="7a7d3-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7a7d3-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


