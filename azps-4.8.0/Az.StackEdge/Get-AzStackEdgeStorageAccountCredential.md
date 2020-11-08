---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261561"
---
# <span data-ttu-id="4f73c-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4f73c-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="4f73c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f73c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f73c-103">Hämtar autentiseringsuppgifterna för lagrings kontot som motsvarar lagrings kontot på enheten.</span><span class="sxs-lookup"><span data-stu-id="4f73c-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="4f73c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f73c-104">SYNTAX</span></span>

### <span data-ttu-id="4f73c-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f73c-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f73c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f73c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f73c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f73c-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f73c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f73c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="4f73c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f73c-109">DESCRIPTION</span></span>
<span data-ttu-id="4f73c-110">Cmdleten **Get-AzStackEdgeStorageAccountCredential** hämtar autentiseringsuppgifterna för lagrings kontot för motsvarande lagrings konto på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="4f73c-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="4f73c-111">Du kan ange parametrar för namn, resurs grupp namn och enhets namn för att få information om en viss autentiseringsuppgift för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4f73c-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="4f73c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f73c-112">EXAMPLES</span></span>

### <span data-ttu-id="4f73c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f73c-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="4f73c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f73c-114">PARAMETERS</span></span>

### <span data-ttu-id="4f73c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f73c-115">-DefaultProfile</span></span>
<span data-ttu-id="4f73c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f73c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f73c-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="4f73c-117">-DeviceName</span></span>
<span data-ttu-id="4f73c-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="4f73c-118">Device Name</span></span>

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

### <span data-ttu-id="4f73c-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4f73c-119">-DeviceObject</span></span>
<span data-ttu-id="4f73c-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="4f73c-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="4f73c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f73c-121">-Name</span></span>
<span data-ttu-id="4f73c-122">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="4f73c-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f73c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f73c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f73c-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4f73c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4f73c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f73c-125">-ResourceId</span></span>
<span data-ttu-id="4f73c-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f73c-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="4f73c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f73c-127">CommonParameters</span></span>
<span data-ttu-id="4f73c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f73c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f73c-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f73c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f73c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f73c-130">INPUTS</span></span>

### <span data-ttu-id="4f73c-131">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4f73c-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="4f73c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f73c-132">OUTPUTS</span></span>

### <span data-ttu-id="4f73c-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4f73c-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="4f73c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f73c-134">NOTES</span></span>

## <span data-ttu-id="4f73c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f73c-135">RELATED LINKS</span></span>
