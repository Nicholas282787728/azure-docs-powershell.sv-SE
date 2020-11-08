---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263462"
---
# <span data-ttu-id="fb34a-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb34a-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="fb34a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb34a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb34a-103">Hämtar Restiction-konfiguration för ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb34a-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="fb34a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb34a-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb34a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb34a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb34a-106">Cmdleten **Get-AzWebAppAccessRestrictionConfig** får åtkomst begränsnings konfiguration för Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb34a-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="fb34a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb34a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb34a-108">Exempel 1: Hämta en begränsning för åtkomst begränsningar för webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="fb34a-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="fb34a-109">Det här kommandot får åtkomst begränsningen config för ett webb program som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="fb34a-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="fb34a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb34a-110">PARAMETERS</span></span>

### <span data-ttu-id="fb34a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb34a-111">-DefaultProfile</span></span>
<span data-ttu-id="fb34a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb34a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb34a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb34a-113">-Name</span></span>
<span data-ttu-id="fb34a-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="fb34a-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb34a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb34a-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb34a-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fb34a-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb34a-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="fb34a-117">-SlotName</span></span>
<span data-ttu-id="fb34a-118">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="fb34a-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb34a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb34a-119">CommonParameters</span></span>
<span data-ttu-id="fb34a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb34a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb34a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb34a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb34a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb34a-122">INPUTS</span></span>

### <span data-ttu-id="fb34a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fb34a-123">System.String</span></span>

## <span data-ttu-id="fb34a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb34a-124">OUTPUTS</span></span>

### <span data-ttu-id="fb34a-125">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb34a-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="fb34a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb34a-126">NOTES</span></span>

## <span data-ttu-id="fb34a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb34a-127">RELATED LINKS</span></span>

[<span data-ttu-id="fb34a-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="fb34a-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="fb34a-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="fb34a-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="fb34a-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="fb34a-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
