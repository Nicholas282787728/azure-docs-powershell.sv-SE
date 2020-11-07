---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 08a4ab0f0d937f06ee0ac958aa57a2f0eed5e4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755208"
---
# <span data-ttu-id="d6466-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="d6466-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="d6466-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6466-102">SYNOPSIS</span></span>
<span data-ttu-id="d6466-103">Hämta loggarna för en container instans i en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="d6466-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6466-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6466-104">SYNTAX</span></span>

### <span data-ttu-id="d6466-105">GetContainerInstanceLogByNamesParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d6466-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6466-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="d6466-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6466-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="d6466-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6466-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6466-108">DESCRIPTION</span></span>
<span data-ttu-id="d6466-109">Cmdleten **Get-AzureRmContainerInstanceLog** hämtar loggarna för en behållare i en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="d6466-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="d6466-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6466-110">EXAMPLES</span></span>

### <span data-ttu-id="d6466-111">Exempel 1: Hämta pilslut för en behållar förekomst</span><span class="sxs-lookup"><span data-stu-id="d6466-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d6466-112">Hämta loggen från `container1` i behållar gruppen `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d6466-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="d6466-113">Som standard returnerar den det 4 MB loggnings innehåll.</span><span class="sxs-lookup"><span data-stu-id="d6466-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="d6466-114">Exempel 2: Hämta loggen för en behållar instans med samma namn som behållar gruppen</span><span class="sxs-lookup"><span data-stu-id="d6466-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d6466-115">Hämta loggen från `mycontainer` i behållar gruppen `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d6466-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="d6466-116">Som standard returnerar den det 4 MB loggnings innehåll.</span><span class="sxs-lookup"><span data-stu-id="d6466-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="d6466-117">Exempel 3: Hämta sidor med 2 rader i loggen för en behållar instans</span><span class="sxs-lookup"><span data-stu-id="d6466-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="d6466-118">Hämta slut 2 raderna i loggen från `container1` i behållar gruppen `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d6466-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="d6466-119">Exempel 4: Hämta loggen för en container instans i en piped i behållar gruppen</span><span class="sxs-lookup"><span data-stu-id="d6466-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="d6466-120">Hämta loggen från `mycontainer` i piped i behållar gruppen `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="d6466-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="d6466-121">Som standard returnerar den det 4 MB loggnings innehåll.</span><span class="sxs-lookup"><span data-stu-id="d6466-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="d6466-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6466-122">PARAMETERS</span></span>

### <span data-ttu-id="d6466-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="d6466-123">-ContainerGroupName</span></span>
<span data-ttu-id="d6466-124">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6466-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6466-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6466-125">-DefaultProfile</span></span>
<span data-ttu-id="d6466-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6466-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6466-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d6466-127">-InputContainerGroup</span></span>
<span data-ttu-id="d6466-128">Gruppobjektet för en indataenhet.</span><span class="sxs-lookup"><span data-stu-id="d6466-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6466-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6466-129">-Name</span></span>
<span data-ttu-id="d6466-130">Namnet på behållar förekomsten i behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6466-130">The container instance name in the container group.</span></span>
<span data-ttu-id="d6466-131">Standard: samma som namnet på behållar gruppen</span><span class="sxs-lookup"><span data-stu-id="d6466-131">Default: the same as the container group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6466-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6466-132">-ResourceGroupName</span></span>
<span data-ttu-id="d6466-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d6466-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6466-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6466-134">-ResourceId</span></span>
<span data-ttu-id="d6466-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d6466-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6466-136">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="d6466-136">-Tail</span></span>
<span data-ttu-id="d6466-137">Antalet rader som ska loggas.</span><span class="sxs-lookup"><span data-stu-id="d6466-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="d6466-138">Om det inte anges, returnerar cmdleten upp till 4 MB ensidig logg</span><span class="sxs-lookup"><span data-stu-id="d6466-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6466-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6466-139">CommonParameters</span></span>
<span data-ttu-id="d6466-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6466-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6466-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6466-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6466-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6466-142">INPUTS</span></span>

### <span data-ttu-id="d6466-143">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d6466-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="d6466-144">Parametrar: InputContainerGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d6466-144">Parameters: InputContainerGroup (ByValue)</span></span>

### <span data-ttu-id="d6466-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d6466-145">System.String</span></span>

## <span data-ttu-id="d6466-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6466-146">OUTPUTS</span></span>

### <span data-ttu-id="d6466-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d6466-147">System.String</span></span>

## <span data-ttu-id="d6466-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6466-148">NOTES</span></span>

## <span data-ttu-id="d6466-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6466-149">RELATED LINKS</span></span>
