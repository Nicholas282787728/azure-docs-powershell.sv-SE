---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523350"
---
# <span data-ttu-id="9c43d-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9c43d-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="9c43d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c43d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c43d-103">Tar bort slut punkter och metadata för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="9c43d-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="9c43d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c43d-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c43d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c43d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c43d-106">Remove-AzEnvironment cmdlet tar bort slut punkter och metadatainformation för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="9c43d-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="9c43d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c43d-107">EXAMPLES</span></span>

### <span data-ttu-id="9c43d-108">Exempel 1: skapa och ta bort en test miljö</span><span class="sxs-lookup"><span data-stu-id="9c43d-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="9c43d-109">Det här exemplet visar hur du skapar en miljö med Add-AzEnvironment och hur du tar bort miljön med Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="9c43d-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="9c43d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c43d-110">PARAMETERS</span></span>

### <span data-ttu-id="9c43d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c43d-111">-DefaultProfile</span></span>
<span data-ttu-id="9c43d-112">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c43d-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c43d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c43d-113">-Name</span></span>
<span data-ttu-id="9c43d-114">Anger namnet på den miljö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9c43d-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="9c43d-115">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="9c43d-115">-Scope</span></span>
<span data-ttu-id="9c43d-116">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="9c43d-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43d-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c43d-117">-Confirm</span></span>
<span data-ttu-id="9c43d-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c43d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c43d-119">-WhatIf</span></span>
<span data-ttu-id="9c43d-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c43d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c43d-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c43d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c43d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c43d-122">CommonParameters</span></span>
<span data-ttu-id="9c43d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c43d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c43d-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c43d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c43d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c43d-125">INPUTS</span></span>

### <span data-ttu-id="9c43d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9c43d-126">System.String</span></span>

## <span data-ttu-id="9c43d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c43d-127">OUTPUTS</span></span>

### <span data-ttu-id="9c43d-128">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="9c43d-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="9c43d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c43d-129">NOTES</span></span>

## <span data-ttu-id="9c43d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c43d-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c43d-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9c43d-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="9c43d-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9c43d-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="9c43d-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9c43d-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

