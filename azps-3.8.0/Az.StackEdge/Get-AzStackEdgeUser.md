---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088778"
---
# <span data-ttu-id="9ca5f-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9ca5f-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="9ca5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ca5f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca5f-103">Hämtar de konfigurerade användarna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="9ca5f-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="9ca5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ca5f-104">SYNTAX</span></span>

### <span data-ttu-id="9ca5f-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9ca5f-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca5f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca5f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca5f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca5f-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca5f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca5f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9ca5f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ca5f-109">DESCRIPTION</span></span>
<span data-ttu-id="9ca5f-110">Cmdleten **Get-AzStackEdgeUser** visar de användare som har kon figurer ATS för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="9ca5f-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="9ca5f-111">Du kan nämna namnet i parametrar för att få information om en viss användare.</span><span class="sxs-lookup"><span data-stu-id="9ca5f-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="9ca5f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ca5f-112">EXAMPLES</span></span>

### <span data-ttu-id="9ca5f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ca5f-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="9ca5f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ca5f-114">PARAMETERS</span></span>

### <span data-ttu-id="9ca5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca5f-115">-DefaultProfile</span></span>
<span data-ttu-id="9ca5f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca5f-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="9ca5f-117">-DeviceName</span></span>
<span data-ttu-id="9ca5f-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="9ca5f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca5f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9ca5f-119">-DeviceObject</span></span>
<span data-ttu-id="9ca5f-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="9ca5f-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca5f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ca5f-121">-Name</span></span>
<span data-ttu-id="9ca5f-122">Namnen</span><span class="sxs-lookup"><span data-stu-id="9ca5f-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ca5f-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9ca5f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca5f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca5f-125">-ResourceId</span></span>
<span data-ttu-id="9ca5f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca5f-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca5f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca5f-127">CommonParameters</span></span>
<span data-ttu-id="9ca5f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca5f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca5f-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ca5f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca5f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ca5f-130">INPUTS</span></span>

### <span data-ttu-id="9ca5f-131">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9ca5f-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="9ca5f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ca5f-132">OUTPUTS</span></span>

### <span data-ttu-id="9ca5f-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9ca5f-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="9ca5f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ca5f-134">NOTES</span></span>

## <span data-ttu-id="9ca5f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ca5f-135">RELATED LINKS</span></span>
