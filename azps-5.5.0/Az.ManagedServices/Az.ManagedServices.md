---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221559"
---
# Az.ManagedServices-modul
## Beskrivning
Den här funktionen används av kunder med hanterade tjänsteleverantörer (MSP). Kunder ger en MSP möjlighet att hantera sin prenumeration eller resursgrupp. Förutom att bevilja åtkomst kan kunden också ta bort åtkomst eller visa befintlig åtkomst. MsP kan visa listan över kunder som har beviljat dem åtkomst till prenumerationer. Det är två objekt inblandade i den här processen: En registreringsdefinition som identifierar den MSP och de rolldefinitioner som tilldelas användarna av MSP. MSP kan alternativt definiera det här objektet med en hanterad tjänst marketplace som erbjuder Access-tilldelningar som associerar en prenumeration med definitionen.

## Az.ManagedServices-cmdlets
### [Get-AzManagedServicesAssignment](Get-AzManagedServicesAssignment.md)
Får en särskild registreringstilldelning eller en lista över registreringstilldelningarna.

### [Get-AzManagedServicesDefinition](Get-AzManagedServicesDefinition.md)
Får en specifik registreringsdefinition eller en lista med registreringsdefinitioner.

### [New-AzManagedServicesAssignment](New-AzManagedServicesAssignment.md)
Skapar eller uppdaterar en registreringstilldelning.

### [New-AzManagedServicesDefinition](New-AzManagedServicesDefinition.md)
Skapar eller uppdaterar en registreringsdefinition.

### [Remove-AzManagedServicesAssignment](Remove-AzManagedServicesAssignment.md)
Tar bort en registreringstilldelning.

### [Remove-AzManagedServicesDefinition](Remove-AzManagedServicesDefinition.md)
Tar bort en registreringsdefinition.
